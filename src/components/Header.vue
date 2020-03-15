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
                        <img src="../assets/img/header/menu_aboutus.png" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/guideline">
                        <img src="../assets/img/header/menu_guideline.png" alt="" />
                    </router-link>
                </li>
                <li>
                    <router-link to="/product">
                        <img src="../assets/img/header/menu_product.png" alt="" />
                    </router-link>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped src="@/assets/css/header.scss" lang="scss">
</style>
