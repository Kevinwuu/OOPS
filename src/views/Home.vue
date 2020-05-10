<template>
  <div class="home">
      <img id="bubble" class="wow animated fadeInDown" src="../assets/img/home/bubble.png" alt="">
      <div class="oops_area">
        <img class="oops_logo" src="../assets/img/home/oops.png" alt="">
      </div>
      <div class="aboutus_area">
          <img class="aboutus_text wow animated fadeInLeft" src="../assets/img/home/text_aboutus.png" alt="" />
          <img id="about" src="../assets/img/home/img_about.jpg" class="wow animated fadeIn" alt="">
      </div>
      <div class="product_area">
          <img class="product_text wow animated fadeInUp" src="../assets/img/home/text_product.png" alt="" />
          <img id="product" src="../assets/img/home/img_product_desc.jpg" class="wow animated fadeInLeft" alt="">
      </div>
      <div class="guideline_area">
          <img class="guideline_text" src="../assets/img/home/text_guideline.png" alt="" />
          <img id="guideline" src="../assets/img/home/img_guideline.jpg" alt="" class="wow animated fadeInRight"/>
      </div>
      <div class="follow_us_area">
        <img class="follow_us_text wow animated fadeInUp" src="../assets/img/home/followus.png" alt="">
        <div class="ig_area">
            <img v-for="path in IG.source" :key="path.id" :src="path" @click="handleIgClick" alt="">
        </div>
      </div>
  </div>
</template>

<script>
import IG_01 from '@/assets/img/home/followUs/IG_01.jpg'
import IG_02 from '@/assets/img/home/followUs/IG_02.jpg'
import IG_03 from '@/assets/img/home/followUs/IG_03.jpg'
import IG_04 from '@/assets/img/home/followUs/IG_04.jpg'
import IG_05 from '@/assets/img/home/followUs/IG_05.jpg'
import IG_06 from '@/assets/img/home/followUs/IG_06.jpg'

export default {
  name: 'Home',
  data() {
    return {
      IG: {
        source: [IG_01, IG_02, IG_03, IG_04, IG_05, IG_06],
        link: 'https://www.instagram.com/oops20192020/'
      }
    }
  },
  methods: {
    handleIgClick() {
      window.open(this.IG.link, "_blank")
    }
  }
}
</script>
