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
  background-color rgba(240, 240, 240, 0.15)
  color red
  height 50px
.buttonmenu
    margin-right 20px
    margin-top 14px
    width 30px
    float right
    &:hover
      .buttonmenustick
       background-color #FF775F
       color white
     &:active
      .buttonmenustick
       box-shadow 0 0 15px #FFD0C7
       transition all .2s
.buttonmenustick
     height 7px
     width 30px
     border-radius 20px
     margin-bottom 1px
     background-color #FF9683
</style>
