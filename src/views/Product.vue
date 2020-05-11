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
            <img id="tissue_paper" class="wow animated slideInDown" data-wow-duration="1.8s" data-wow-delay="0.8s" src="../assets/img/product/tissue_body.png" alt="">
            <div class="product_field">
              <div class="product_item" v-for="item in product" :key="item.id">
                <img :src="item.src[0]" :alt="item.title" />
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
          <Carousel :path="selectedItem.src" />
        </div>

        <v-card-text >
          <p v-html="selectedItem.desc"></p>
        </v-card-text>

        <v-card-actions>
          <v-btn @click="toggleDialog">
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
import Tumbler01 from '@/assets/img/product/300ml_01.jpg'
import Squeeze from '@/assets/img/product/600ml.jpg'
import Squeeze01 from '@/assets/img/product/600ml_01.jpg'
import Pour from '@/assets/img/product/1000ml.jpg'
import Pour01 from '@/assets/img/product/1000ml_01.jpg'
import Supply from '@/assets/img/product/supply.jpg'
import Supply01 from '@/assets/img/product/supply_01.jpg'
import Box from '@/assets/img/product/box.jpg'
import Box01 from '@/assets/img/product/box_01.jpg'

import Carousel from '@/components/Carousel.vue'

export default {
  name: 'Product',
  data() {
    return {
      dialog: false,
      content:[`
        原料：鶴岡文旦萃取液 純水 椰子油皂化物 椰子粉 月桂基葡萄糖苷 礦物鹽晶</br>
        檸檬酸 蘆薈萃取液</br>
        用途：衛浴 廚房 地板清潔</br>`
        ,`
        功效：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>
        有效日期：未開封2年，開封1年</br></br>

        Made in TAiwan</br></br>

        請給予安全舒適的環境，以避免產品發酵變質，越清越不乾淨</br>
        本產品強烈建議頻繁使用，不要問為什麼，因為他是天然的</br>
        有沈澱的狀況是常態，不怕不健康，只怕你不用他`],
      selectedItem:{
        title:'',
        src: [],
        desc: '',
        usage: ''
      },
      product: [
        {
          title: `
            倒來倒去（300ml)</br>
            Tumbler`,
          src: [Tumbler, Tumbler01],
          link: 'https://shopee.tw/%E5%80%92%E4%BE%86%E5%80%92%E5%8E%BB-300ml%E6%B8%85%E6%BD%94%E5%8A%91-i.471092.6430163656',
          desc: '全天然清潔劑</br>',
          usage: '使用方式：躺著擠趴著擠不如倒著擠</br>'
        },
        {
          title: `
            擠我擠我（600ml)</br>
            Squeeze Me`,
          src: [Squeeze, Squeeze01],
          link: 'https://shopee.tw/%E6%93%A0%E6%88%91%E6%93%A0%E6%88%91-600ml%E6%B8%85%E6%BD%94%E5%8A%91-i.471092.3730261619',
          desc: '全天然清潔劑</br>',
          usage: '使用方式：好擠好擠，那就用力擠出來</br>'
        },
        {
          title: `
            你倒了嗎（1000ml)</br>
            Pour?`,
          src: [Pour, Pour01],
          link: 'https://shopee.tw/%E4%BD%A0%E5%80%92%E4%BA%86%E5%97%8E-1000ml%E6%B8%85%E6%BD%94%E5%8A%91-i.471092.6130166134',
          desc: '全天然清潔劑</br>',
          usage: '使用方式：速速帶走污漬不傷身，還能替你減少殘留的毒素，有效清潔在這裡</br>'
        },
        {
          title: `
            補給小站</br>
            Supply Station`,
          src: [Supply, Supply01],
          link: 'https://shopee.tw/%E8%A3%9C%E7%B5%A6%E5%B0%8F%E7%AB%99-1000ml%E8%A3%9C%E5%85%85%E5%8C%85-i.471092.4130168384',
          desc: '全天然清潔劑補充</br>',
          usage: '使用方式： 還不簡單，拿起來倒出來，結束</br>'
        },
        {
          title: `
            柚柚三兄弟</br>
            Hey!Bro`,
          src: [Box, Box01],
          link: 'https://shopee.tw/%E6%9F%9A%E6%9F%9A%E4%B8%89%E5%85%84%E5%BC%9F-%E7%A6%AE%E7%9B%92%E6%B8%85%E6%BD%94%E5%8A%91-i.471092.3830263754',
          desc: '全天然清潔劑補充</br>',
          usage: '使用方式：帶我們見世面，保證你顏面都在</br>'
        }
      ]
    }
  },
  methods: {
    handleDetailClick(data) {
      let { title, src, desc, usage, link } = data
      let name = title.split('</br>')[0]

      this.selectedItem.title = name
      this.selectedItem.src = src
      this.selectedItem.desc = desc + this.content[0] + usage + this.content[1]
      this.selectedItem.link = link
    },
    handleGoToStoreClick() {
      window.open(this.selectedItem.link, "_blank")
    },
    toggleDialog() {
      this.dialog = !this.dialog
    }
  },
  components: {
    Carousel
  }
}
</script>
