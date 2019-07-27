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
      <h1>ДАРЬЯ ПОДОЛЬНАЯ</h1>
      <h2>ФОТОГРАФ</h2>
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
html
  height 100%
  overflow hidden
@font-face
  font-family 'Roboto-Black'
  src url('./assets/fonts/Roboto-Black.ttf')
@font-face
  font-family 'Raleway-SemiBold'
  src url('./assets/fonts/Raleway-SemiBold.ttf')
body
  margin 0px
  padding 0px
  perspective 1px
  transform-style preserve-3d
  overflow-y scroll
  overflow-x hidden
  width 100vw
  height 100vh
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  background-size cover
  background-position center
  height 100vh
  width 100vw
  position absolute
.contentBox
  box-sizing border-box
  min-height 100vh
  text-align center
  padding-top 30%
  transform-style preserve-3d
  width 100vw
  color #fff
  font-family Raleway-SemiBold
  text-shadow 1px 2px 3px #8A8A8A
  &:before
    content ''
    display block
    position absolute
    left 0
    right 0
    bottom 0
    top 0
    z-index -1
    transform-origin center
    min-height 100vh
    background-image url(./assets/photo/1.jpg)
    background-repeat no-repeat
    background-size cover
    background-position center center
    transform translateZ(-1px) scale(2)
  h1
    margin-top -100px
    &:after
      position absolute
      content ""
      height 2px
      background-color #fff
      width 260px
      display block
      left 50%
      -webkit-transform translate(-50%,0)
      -ms-transform translate(-50%,0)
      transform translate(-50%,0)
  h2
    margin-top -20px
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
.headerBox
  position relative
  z-index 1

.fade-enter-active, .fade-leave-active
  transition opacity .4s

.fade-enter, .fade-leave-to
  opacity 0
</style>
