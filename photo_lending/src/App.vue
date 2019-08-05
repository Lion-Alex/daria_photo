<template>
  <div id="app">
    <div class="contentBoxOne">
      <h1>ДАРЬЯ ПОДОЛЬНАЯ</h1>
      <h2>ФОТОГРАФ</h2>
    </div>
  <div class="contentBoxTwo">
    <h1>ДАРЬЯ ПОДОЛЬНАЯ</h1>
    <h2>ФОТОГРАФ</h2>
    <div class="cards">
      <div class="card">
        <div class="card-header">
          <h4 class="my-0 font-weight-normal">Enterprise</h4>
        </div>
        <div class="card-body">
          <h1 class="card-title pricing-card-title">$29 <small class="text-muted">/ mo</small></h1>
          <ul class="list-unstyled mt-3 mb-4">
            <li>30 users included</li>
            <li>15 GB of storage</li>
            <li>Phone and email support</li>
            <li>Help center access</li>
          </ul>
          <a href="#enterprise" class="btn btn-lg btn-block btn-primary">More info</a>
        </div>
      </div>
      <div class="card">
        <div class="card-header">
          <h4 class="my-0 font-weight-normal">Enterprise</h4>
        </div>
        <div class="card-body">
          <h1 class="card-title pricing-card-title">$29 <small class="text-muted">/ mo</small></h1>
          <ul class="list-unstyled mt-3 mb-4">
            <li>30 users included</li>
            <li>15 GB of storage</li>
            <li>Phone and email support</li>
            <li>Help center access</li>
          </ul>
          <a href="#enterprise" class="btn btn-lg btn-block btn-primary">More info</a>
        </div>
      </div>
      <div class="card">
        <div class="card-header">
          <h4 class="my-0 font-weight-normal">Enterprise</h4>
        </div>
        <div class="card-body">
          <h1 class="card-title pricing-card-title">$29 <small class="text-muted">/ mo</small></h1>
          <ul class="list-unstyled mt-3 mb-4">
            <li>30 users included</li>
            <li>15 GB of storage</li>
            <li>Phone and email support</li>
            <li>Help center access</li>
          </ul>
          <a href="#enterprise" class="btn btn-lg btn-block btn-primary">More info</a>
        </div>
      </div>
    </div>
  </div>
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
  </div>
</template>

<script>
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
.contentBoxOne
  box-sizing border-box
  min-height 100vh
  text-align center
  padding-top 20%
  transform-style preserve-3d
  width 100vw
  color #fff
  font-family Raleway-SemiBold
  text-shadow 1px 2px 3px #8A8A8A
  &:before
    content ''
    display block
    position absolute
    padding 0
    left 0
    right 0
    bottom 0
    top 0
    z-index -1
    transform-origin center
    min-height inherit
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
.contentBoxTwo
  box-sizing border-box
  min-height 100vh
  background-color tomato
  padding-top 20%
  width 100vw
  transform-style preserve-3d
  color #fff
  font-family Raleway-SemiBold
  text-shadow 1px 2px 3px #8A8A8A
  &:before
    content ''
    display block
    position absolute
    padding 0
    left 0
    right 0
    bottom 0
    top 0
    z-index -1
    background-image url(./assets/photo/2.jpg)
    transform-origin center
.cards
  display flex
  justify-content space-evenly
.card
  background-color rgba(0, 0, 0, .6)
  border-radius 10%
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

.Box
  background-color tomato
.clear
  clear both
</style>
