<template>
  <div id="app">
    <!-- Шапка -->
    <div class="headerBox">
      <nav-box></nav-box>
    </div>
    <!-- Меню -->
    <div class="navBox">
    </div>
    <!-- Контент -->
    <div class="contentBox">
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
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
  components: {
    HelloWorld,
    navBox
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
</style>
