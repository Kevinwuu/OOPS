<template>
    <footer>
        <div class="social_media">
            <!-- <img src="img/footer/text_social_websites.png" alt="" /> -->
            <img src="../assets/img/footer/text_social_websites.png" alt="" />
        </div>
        <div class="nav_link">
            <ul>
                <li>
                    <img src="../assets/img/footer/text_index.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/footer/text_aboutus.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/footer/text_guideline.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/footer/text_guideline.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/footer/text_guideline.png" alt="" />
                </li>
            </ul>
        </div>
        <div class="contact">
            <ul>
                <li>
                    <img src="../assets/img/footer/text_address.png" alt="" />
                    <p>
                        <img src="../assets/img/footer/text_address_info.png" alt="" />
                    </p>
                </li>
                <li>
                    <img src="../assets/img/footer/text_phone.png" alt="" />
                    <p>
                        <img src="../assets/img/footer/text_phone_number.png" alt="" />
                    </p>
                </li>
                <li>
                    <img src="../assets/img/footer/text_phone.png" alt="" />
                    <p>
                        <img src="../assets/img/footer/text_phone_number.png" alt="" />
                    </p>
                </li>
            </ul>
        </div>
        <div id="logo">
            <router-link to="/">
                <img src="../assets/img/logo.png" alt="" />
            </router-link>
        </div>
    </footer>
</template>

<script>
// import '@/assets/css/footer.css'
export default {
  name: 'Footer',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped src="@/assets/css/footer.scss" lang="scss">

</style>
