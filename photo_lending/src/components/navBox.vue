<template>
  <header>
    <div class="columnLabel" href="#">
      <a href="#">Daria Photo</a></div>
    <div class="columnNav">
      <ul>
        <li><a href="#">Главная</a></li>
        <li><a href="#">Услуги</a></li>
        <li><a href="#">Портфолио</a></li>
        <li><a href="#">О фотографе</a></li>
        <li><a href="#">Контакты</a></li>
      </ul>
    </div>
    <div class="columnOrder">
      <div class="CallNumber"><div class="Call" href="#">8-000-000-00-00</div></div>
      <button class="buttonOrder">Сделать заказ</button>
    </div>
  </header>
</template>
<script>
export default {
  name: 'navBar',
  data () {
    return {
      menuflag: false
    }
  },
  methods: {},
  components: {}
}
</script>
<style lang="stylus">
@font-face
  font-family 'Hanging_Letters'
  src url('./../assets/fonts/Hanging_Letters.ttf')
@font-face
  font-family 'Roboto-Black'
  src url('./../assets/fonts/Roboto-Black.ttf')
header
  position fixed
  width 100vw
  z-index 10000
  background-color white
  background-position center
  background-repeat no-repeat
  background-size cover
  display flex
  flex-direction row
  justify-content space-between
  .columnLabel
    flex-direction row
    flex-basis 15%
    display flex
    justify-content space-evenly
    a
      color red
      font-family Hanging_Letters

  .columnNav
    flex-direction row
    flex-basis 50%
    ul
      display flex
      justify-content space-evenly
      flex-direction row
      list-style-type none
      li
        min-width 88px
        a
          text-decoration none
          color #535458
          font-family Roboto-Black
  .columnOrder
    flex-direction row
    flex-basis 20%
    display flex
    .buttonOrder
      flex-basis 50%
      cursor pointer
    .CallNumber
      flex-basis 50%
      display flex
      justify-content center
      flex-direction column
      text-align center
      .Call
        cursor pointer
</style>
