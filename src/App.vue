<template>
    <v-app id="app">
        <Header />
          <transition name="fade" mode="out-in">
            <router-view />
          </transition>
        <Footer />
    </v-app>
</template>
<script>
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>
<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>
