<template>
  <div id="app">
    <!-- Шапка -->
    <div class="headerBox">
      <nav-box @openmenu="opensmenu"></nav-box>
    </div>
    <!-- Меню -->
    <div class="contentfull">
    <div class="navBox" v-if="this.menuflags">
      <ul>
        <li><a href="#?">Home</a></li>
        <li><a href="#?">About</a></li>
        <li><a href="#?">Clients</a></li>
        <li><a href="#?">Contact Us</a></li>
      </ul>
    </div>
    <!-- Контент -->
    <div class="contentBox">
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
    </div>
    <!-- Подвал -->
    <div class="footerbox"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import navBox from './components/navBox.vue'
import barBox from './components/barBox.vue'

export default {
  name: 'app',
  data () {
    return {
      menuflags: false
    }
  },
  methods: {
    opensmenu (menuflag) {
      this.menuflags = menuflag
    }
  },
  components: {
    HelloWorld,
    navBox,
    barBox
  }
}
</script>

<style lang="stylus">
body
  margin 0px
  width 100vw
  height 100vh
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  background-image (url(./assets/photo/1.jpg))
  background-size cover
  height 100%
  width 100%
  position absolute
.navBox
  position absolute
  z-index 2
  background-color rgba(240, 240, 240, 0.15)
  width 100%
  height 100%
a
  float left
</style>
