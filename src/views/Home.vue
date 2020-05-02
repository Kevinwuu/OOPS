<template>
  <div class="home">
      <img id="bubble" class="wow animated slideInDown" src="../assets/img/home/bubble.png" alt="">
      <div class="oops">
        <img src="../assets/img/home/oops.png" alt="">
      </div>
      <div class="aboutus">
          <img class="wow animated fadeInLeft" src="../assets/img/home/text_aboutus.png" alt="" />
          <img id="about" src="../assets/img/home/img_about.jpg" class="wow animated fadeIn" alt="">
      </div>
      <div class="product">
          <img class="product_desc wow animated fadeInUp" src="../assets/img/home/text_product.png" alt="" />
          <img id="product" src="../assets/img/home/img_product_desc.jpg" class="wow animated fadeInLeft" alt="">
      </div>
      <div class="guideline">
          <img class="guideline_desc" src="../assets/img/home/text_guideline.png" alt="" />
          <img id="guideline" src="../assets/img/home/img_guideline.jpg" alt="" class="wow animated fadeInRight"/>
      </div>
      <div class="follow_us">
        <img class="follow_us_text wow animated fadeInUp" src="../assets/img/home/followus.jpg" alt="">
        <div class="ig_image_area">
          <a v-for="path in IG.source" :key="path.id" :href="IG.link" target="_blank">
            <img :src="path" alt="">
          </a>
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
      // IG_img: [IG_01, IG_02, IG_03, IG_04, IG_05, IG_06],
      // IG_link: 'https://www.instagram.com/oops20192020/'
    }
  }
}
</script>

<style lang="scss" src="@/assets/css/home.scss" scoped>
</style>
