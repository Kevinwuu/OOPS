<template>
  <footer>
    <div class="social_media">
      <div>
        <img src="../assets/img/footer/text_social_websites.png" alt="" />
      </div>
      <div class="social_icon">
        <a
          v-for="item in social"
          :href="item.link"
          :key="item.id"
          target="_blank"
        >
          <img :src="item.path" alt="" />
        </a>
      </div>
    </div>
    <div class="nav_link">
      <ul>
        <li v-for="item in menu" :key="item.id">
          <router-link :to="item.path">
            <img :src="item.src" alt="" />
          </router-link>
        </li>
      </ul>
    </div>
    <div class="contact">
      <ul>
        <li v-for="item in contact" :key="item.id">
          <img :src="item.title" alt="" />
          <p>
            <img :src="item.info" alt="" />
          </p>
        </li>
      </ul>
    </div>
    <div class="logo">
      <router-link to="/">
        <img src="../assets/img/logo.png" alt="" />
      </router-link>
    </div>
  </footer>
</template>

<script>
import Index from '@/assets/img/footer/text_index.png'
import AboutUs from '@/assets/img/footer/text_aboutus.png'
import Guideline from '@/assets/img/footer/text_guideline.png'
import Product from '@/assets/img/footer/text_product.png'

import Line from '@/assets/img/footer/LINE.png'
import Youtube from '@/assets/img/footer/YT.png'
import Facebook from '@/assets/img/footer/FB.png'
import Instagram from '@/assets/img/footer/IG.png'

import Address from '@/assets/img/footer/text_address.png'
import Phone from '@/assets/img/footer/text_phone.png'
import Email from '@/assets/img/footer/text_email.png'
import AddressInfo from '@/assets/img/footer/text_address_info.png'
import PhoneInfo from '@/assets/img/footer/text_phone_info.png'
import EmailInfo from '@/assets/img/footer/text_email_info.png'

export default {
  name: 'Footer',
  data() {
    return {
      message: 'xdd',
    //   menu: [Index, AboutUs, Guideline, Product],
      menu: [
          {path:'/', src:Index},
          {path:'/aboutus',src:AboutUs},
          {path:'/guideline',src:Guideline},
          {path:'/product',src:Product}
    ],
      social: [
        { link: 'https://lin.ee/gk9O1wC', path: Line },
        {
          link:
            'https://m.youtube.com/channel/UCQR-Wq0hiRPERUcKjs-y_Eg/featured',
          path: Youtube
        },
        {
          link:
            'https://m.facebook.com/Oops2019-110233197082200/?modal=admin_todo_tour',
          path: Facebook
        },
        {
          link: 'https://www.instagram.com/_oops2019/?hl=zh-tw',
          path: Instagram
        }
      ],
      contact: [
        { title: Address, info: AddressInfo },
        { title: Phone, info: PhoneInfo },
        { title: Email, info: EmailInfo }
      ]
    }
  }
}
</script>

<style scoped src="@/assets/css/footer.scss" lang="scss"></style>
