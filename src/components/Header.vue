<template>
    <header>
        <div class="logo">
            <router-link to="/">
                <img src="../assets/img/logo.png" alt="" />
            </router-link>
        </div>
        <div class="nav">
            <ul>
                <li>
                    <router-link to="/about">
                        <img :src="imgSrc[0]" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/guideline">
                        <img :src="imgSrc[1]" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/product">
                        <img :src="imgSrc[2]" alt="" />
                    </router-link>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
import AboutUs from '@/assets/img/header/menu_aboutus.png'
import Guideline from '@/assets/img/header/menu_guideline.png'
import Product from '@/assets/img/header/menu_product.png'

export default {
  name: 'Header',
  data () {
    return {
      imgSrc: [AboutUs, Guideline, Product]
    }
  }
}
</script>

<style scoped src="@/assets/css/header.scss" lang="scss">
</style>
