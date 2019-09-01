<template>
  <div class="photocarousel">
      <div class="buttonArea">
          <button class="buttonLeft"></button>
          <button class="buttonRight"></button>
      </div>
      <div class="infoarea">
          <div class="textbuttarea">
            <h1>Фотограф от бога</h1>
            <button></button>
          </div>
          <div></div>
      </div>
  </div>
</template>
<script>
export default {
  name: 'carousel',
  data () {
    return {}
  },
  methods: {},
  components: {}
}
</script>
<style lang="stylus">
@font-face
  font-family 'Hanging_Letters'
  src url('./../assets/fonts/Hanging_Letters.ttf')
.photocarousel
    background-image url('./../assets/photo/carousel/3.jpg')
    position relative
    z-index 0
    background-position center
    background-repeat no-repeat
    background-size cover
    min-height 80vh
    display flex
    flex-direction column
    justify-content center
    .buttonArea
        .buttonLeft
            float left
            width 30px
            height 40px
        .buttonRight
            float right
            width 30px
            height 40px
    .infoarea
        display flex
        flex-direction row
        justify-content space-between
        .textbuttarea
            flex-basis 50%
            align-items center
            flex-direction column
            display flex
            h1
                color white
            button
                height 50px
                width 100px
                margin-left 200px
</style>
