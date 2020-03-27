<template>
    <footer>
        <div class="social_media">
            <div>
                <img src="../assets/img/footer/text_social_websites.png" alt="" />
            </div>
            <div class="social_icon">
                <img src="../assets/img/footer/LINE.png" alt="">
                <img src="../assets/img/footer/YT.png" alt="">
                <img src="../assets/img/footer/FB.png" alt="">
                <img src="../assets/img/footer/IG.png" alt="">
            </div>
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
                    <img src="../assets/img/footer/text_product.png" alt="" />
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
                    <img src="../assets/img/footer/text_email.png" alt="" />
                    <p>
                        <img src="../assets/img/footer/text_email_info.png" alt="" />
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
export default {
  name: 'Footer',
  props: {
    msg: String
  }
}
</script>

<style scoped src="@/assets/css/footer.scss" lang="scss">
</style>
