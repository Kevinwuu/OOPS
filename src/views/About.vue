<template>
<div class="about">
  <div class="water">
    <img id="water_tube" src="../assets/img/aboutus/water_tube.png" alt="">
    <img id="water_bubble" src="../assets/img/aboutus/water_bubble.png" alt=""  data-aos="fade-down" >
    <div class="content">
      <div class="content_desc">
        <h1 v-html="title"></h1>
        <h2 v-html="slogan"></h2>
        <p v-html="desc"></p>
      </div>
      <div class="about_icon">
        <img  class="wow animated fadeInDown"  data-wow-delay="2" v-for="icon in icons" :key="icon.id" :src="icon" alt="">
      </div>
      <div class="about_noicon">
        <img  class="wow animated fadeInDown"  data-wow-delay="4" v-for="no_icon in no_icons" :key="no_icon.id" :src="no_icon" alt="">
      </div>
    </div>
  </div>
</div>
</template>

<script>
import Icon1 from '@/assets/img/aboutus/icon/icon1.png'
import Icon2 from '@/assets/img/aboutus/icon/icon2.png'
import Icon3 from '@/assets/img/aboutus/icon/icon3.png'
import Icon4 from '@/assets/img/aboutus/icon/icon4.png'
import Icon5 from '@/assets/img/aboutus/icon/icon5.png'

import NoIcon1 from '@/assets/img/aboutus/icon/No icon1.png'
import NoIcon2 from '@/assets/img/aboutus/icon/No icon2.png'
import NoIcon3 from '@/assets/img/aboutus/icon/No icon3.png'
import NoIcon4 from '@/assets/img/aboutus/icon/No icon4.png'
import NoIcon5 from '@/assets/img/aboutus/icon/No icon5.png'

export default {
  name: 'About',
  data() {
    return {
      title: "好的產品,我們給你",
      slogan:`
        O  optimum 最佳的<br>
        O  omnipotent 無所不能<br>
        P  profession 專業的<br>
        S  safe 安全的<br>
      `,
      desc: `
        因為身邊有好的產品，透過推廣讓更多人知道<br>
        利用設計系的優勢顛覆大家對於清潔劑的印象<br>
        藉由鮮豔的色彩與活潑的調性，來吸引消費者<br>
        想讓同一個世代的年輕人可以正視天然清潔劑<br>
        誰說天然清潔劑只屬於年長者與幼童呢？<br>
        再加上今年初爆發的疫情，大家開始注重清潔<br>
        希望清潔這件事不是因為疫情才選擇去做<br>
        唯有定時清潔才能讓我們身處健康的環境<br>
      `,
      icons: [Icon1,Icon2,Icon3,Icon4,Icon5],
      no_icons: [NoIcon1,NoIcon2,NoIcon3,NoIcon4,NoIcon5]
    }
  }
}
</script>
