<template>
  <div class="bar">
    <div class="buttonmenu" @click="menuon()">
          <div class="buttonmenustick"></div>
          <div class="buttonmenustick"></div>
          <div class="buttonmenustick"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'navBar',
  data () {
    return {
      menuflag: false
    }
  },
  methods: {
    menuon () {
      this.menuflag = !this.menuflag
      this.$emit('openmenu', this.menuflag)
    }
  },
  components: {}
}
</script>
<style lang="stylus">
.bar
  background-color rgba(0, 0, 0, .6)
  color red
  height 50px
.buttonmenu
    border solid 1px
    border-color rgba(255, 255, 255, .7)
    padding 6px
    border-radius 10%
    margin-left 20px
    margin-top 10px
    width 30px
    float left
    &:hover
      border-color #FF775F
      transition all .4s
      .buttonmenustick
       background-color #FF775F
       color white
       transition all .4s
     &:active
      .buttonmenustick
       box-shadow 0 0 15px #FFD0C7
       transition all .2s
.buttonmenustick
     height 3px
     width 30px
     border-radius 20px
     margin-bottom 3px
     margin-top 3px
     background-color rgba(255, 255, 255, .7)
</style>
