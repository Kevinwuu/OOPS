<template>
  <v-carousel
    height="400"
    cycle
    hide-delimiter-background
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
      :src="slides[i]"
    >
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
    props: ['path'],
    data () {
        return {
            slides:this.path,
        }
    },
}
</script>
