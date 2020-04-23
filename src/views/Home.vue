<template>
  <div class="home">
      <div class="oops">
        <img src="../assets/img/home/oops.png" alt="">
      </div>
      <div class="aboutus" data-aos="fade-right">
          <img src="../assets/img/home/text_aboutus.png" alt="" />
          <img id="about" src="../assets/img/home/img_about.jpg" data-aos="fade-left" alt="">
      </div>
      <div class="product" data-aos="fade-up">
          <img src="../assets/img/home/text_product.png" alt="" />
          <img id="product" src="../assets/img/home/img_product_desc.jpg" data-aos="fade-right" alt="">
      </div>
      <div class="guideline">
          <img src="../assets/img/home/text_guideline.png" alt="" />
          <img id="guideline" src="../assets/img/home/img_guideline.jpg" alt="" data-aos="fade-left"/>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Home'
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="@/assets/css/home.scss" scoped>
</style>
