<template>
  <div id="app">
    <!-- Шапка -->
    <div class="headerBox">
      <nav-box @openmenu="opensmenu"></nav-box>
    </div>
    <!-- Меню -->
    <div class="contentfull">
    <transition name="fade">
      <div class="navBox" v-show="this.menuflags" :class="{'open': menuflags}">
        <ul>
          <li><a href="#?">Home</a></li>
          <li><a href="#?">About</a></li>
          <li><a href="#?">Clients</a></li>
          <li><a href="#?">Contact Us</a></li>
        </ul>
      </div>
    </transition>
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
    navBox
  }
}
</script>

<style lang="stylus">
@font-face
  font-family 'Roboto-Black'
  src url('./assets/fonts/Roboto-Black.ttf')
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
  background-position center
  height 100vh
  width 100vw
  position absolute
.navBox
  position absolute
  z-index 2
  height calc(100vh - 50px)
  width 100vw
  background-color rgba(0, 0, 0, .6)
  a
    float left
    text-shadow 2px 2px 0 #000
    text-decoration none
    color rgba(255, 255, 255, .6)
    font 3em Roboto-Black
    display block
  li
    display flex

.fade-enter-active, .fade-leave-active
  transition opacity .4s

.fade-enter, .fade-leave-to
  opacity 0
</style>
