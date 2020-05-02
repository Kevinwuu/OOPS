<template>
    <v-dialog v-model="dialog" width="580">
      <template v-slot:activator="{ on }">
        <div class="product">
          <div class="tissue">
            <img
              class="tissue_head"
              src="../assets/img/product/tissue_head.png"
              alt=""
            />
            <div class="product_field">
              <div class="product_item" v-for="item in product" :key="item.id">
                <img :src="item.src" :alt="item.title" />
                <p v-html="item.title"></p>
                <v-btn v-on="on" @click="handleDetailClick(item)">詳細資訊</v-btn>
              </div>
            </div>
          </div>
        </div>
      </template>

      <v-card>
        <v-card-title class="headline grey lighten-2" primary-title v-html="selectedItem.title">
        </v-card-title>
        <div class="v-card__content">
          <img :src="selectedItem.src" alt="">
        </div>
        <v-card-text v-html="selectedItem.desc">
        </v-card-text>

        <!-- <v-divider></v-divider> -->

        <v-card-actions>
          <v-btn @click="dialog = false">
            <v-icon dark left>mdi-arrow-left</v-icon>
            Back
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn color="red" dark @click="handleGoToStoreClick">
            蝦皮賣場
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>

<script>
import Tumbler from '@/assets/img/product/300ml.jpg'
import Squeeze from '@/assets/img/product/600ml.jpg'
import Pour from '@/assets/img/product/1000ml.jpg'
import Supply from '@/assets/img/product/supply.jpg'
import Box from '@/assets/img/product/box.jpg'

export default {
  name: 'Product',
  data() {
    return {
      dialog: false,
      selectedItem:{
        title:'',
        src: '',
        desc: ''
      },
      product: [
        {
          title: `
            倒來倒去（300ml)</br>
            Tumbler
          `,
          src: Tumbler,
          desc: `
            全天然清潔劑</br>
            原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
            檸檬酸 蘆薈萃取液</br>
            用途：衛浴 廚房 地板清潔</br>
            使用方式：躺著擠趴著擠不如倒著擠</br>
            功效：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
            有效日期：未開封2年，開封1年</br></br>

            Made in TAiwan</br></br>

            請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
            本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
            有沈澱的狀況是常態，不怕不健康，只怕你不用他`
        },
        {
          title: `
            擠我擠我（600ml)</br>
            Squeeze Me
          `,
          src: Squeeze,
          desc: `
            全天然清潔劑</br>
            原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
            檸檬酸 蘆薈萃取液</br>
            用途：衛浴 廚房 地板清潔</br>
            使用方式：好擠好擠，那就用力擠出來</br>
            功效：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
            有效日期：未開封2年，開封1年</br></br>

            Made in TAiwan</br></br>

            請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
            本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
            有沈澱的狀況是常態，不怕不健康，只怕你不用他`
        },
        {
          title: `
            你倒了嗎（1000ml)</br>
            Pour?
          `,
          src: Pour,
          desc: `
            全天然清潔劑</br>
            原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
            檸檬酸 蘆薈萃取液</br>
            用途：衛浴 廚房 地板清潔</br>
            使用方式：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
            有效日期：未開封2年，開封1年</br></br>

            Made in TAiwan</br></br>

            請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
            本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
            有沈澱的狀況是常態，不怕不健康，只怕你不用他`
        },
        {
          title: `
            補給小站</br>
            Supply Station
          `,
          src: Supply,
          desc: `
            全天然清潔劑補充</br>
            原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
            檸檬酸 蘆薈萃取液</br>
            用途：衛浴 廚房 地板清潔</br>
            使用方式： 還不簡單，拿起來倒出來，結束</br>
            功效：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
            有效日期：未開封2年，開封1年</br></br>

            請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
            本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
            有沈澱的狀況是常態，不怕不健康，只怕你不用`
        },
        {
          title: `
            柚柚三兄弟</br>
            Hey!Bro
          `,
          src: Box,
          desc: `
            全天然清潔劑補充</br>
            原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
            檸檬酸 蘆薈萃取液</br>
            用途：衛浴 廚房 地板清潔</br>
            使用方式：帶我們見世面，保證你顏面都在</br>
            功效：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
            有效日期：未開封2年，開封1年</br></br>

            請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
            本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
            有沈澱的狀況是常態，不怕不健康，只怕你不用他`
        }
      ]
    }
  },
  methods: {
    handleDetailClick(data) {
      console.log(data)
      let product_name = data.title.split('</br>')[0]
      this.selectedItem.title = product_name
      this.selectedItem.src = data.src
      this.selectedItem.desc = data.desc
    },
    handleGoToStoreClick() {
      window.open("https://shopee.tw/peggy0223?smtt=0.0.9", "_blank")
    }
  }
}
</script>

<style lang="scss" src="@/assets/css/product.scss" scoped></style>
