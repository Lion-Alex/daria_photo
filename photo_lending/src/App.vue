<template>
  <div id="app">
  <transition name="fade">
      <navBox></navBox>
    </transition>
  <carouselbox></carouselbox>
  </div>
</template>

<script>
import navBox from '@/components/navBox.vue'
import carouselbox from '@/components/carousel.vue'
export default {
  name: 'app',
  data () {
    return {
      menuflags: false
    }
  },
  methods: {},
  components: {
    navBox,
    carouselbox
  }
}
</script>

<style lang="stylus">
@font-face
  font-family 'Roboto-Black'
  src url('./assets/fonts/Roboto-Black.ttf')
@font-face
  font-family 'Raleway-SemiBold'
  src url('./assets/fonts/Raleway-SemiBold.ttf')
body
  margin 0px
</style>
