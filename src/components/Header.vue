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
                        <img src="../assets/img/nav/menu_aboutus.png" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/guideline">
                        <img src="../assets/img/nav/menu_guideline.png" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/product">
                        <img src="../assets/img/nav/menu_product.png" alt="" />
                    </router-link>
                </li>
                <li>
                    <img src="../assets/img/nav/menu_member.png" alt="" />
                </li>
            </ul>
            <div class="account">
                <li>
                    <img src="../assets/img/nav/account.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/nav/logout.png" alt="" />
                </li>
                <li>
                    <img src="../assets/img/nav/cart.png" alt="" />
                </li>
            </div>
        </div>
    </header>
</template>

<script>
// import '@/assets/css/header.css'
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped src="@/assets/css/header.scss" lang="scss">

</style>
