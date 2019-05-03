<template>
  <div class="header">
    城市选择
    <fade-animation>
      <router-link to = "/">
        <div class="iconfont header-back">&#xe624;</div>
      </router-link>
    </fade-animation>
  </div>
</template>

<script>
import FadeAnimation from '../../../common/fade/FadeAnimation'
export default {
  name: 'CityHeader',
  components: {FadeAnimation}
}

</script>

<style lang = "stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    overflow :hidden
    height:$headerHeight
    line-height :$headerHeight
    text-align :center
    color: #fff
    background :$bgColor
    font-size :.32rem
    .header-back
      position :absolute
      top: 0
      left 0
      width :.64rem
      text-align :center
      font-size :.4rem
      color:#fff
</style>
