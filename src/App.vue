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
