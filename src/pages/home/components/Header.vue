<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
    输入城市景点游玩主题
  </div>
    <router-link to = '/city'>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont arrow-icon">&#xe62d;</span>
    </div>
    </router-link>
  </div>

</template>

<script>

export default{
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<!--1rem = html font-size = 50px-->
<!--86px = 0.43rem-->
<style lang = "stylus" scoped>
  /*@import "../../../assets/styles/varibles.styl"*/
  @import "~styles/varibles.styl"
  .header
    display :flex
    line-height: $headerHeight
    background :$bgColor
    color:#fff
    .header-left
      width : .64rem
      float :left
      .back-icon
        text-align:center
        font-size :.4rem
    .header-input
      flex:1
      height :.64rem
      margin-top :.12rem
      margin-left :.2rem
      padding-left :.2rem
      background :#ffffff
      border-radius :.1rem
      color: #ccc
      line-height:.64rem
      text-align :left
    .header-right
      width:1.24rem
      float:right
      text-align :center
      color :#fff
      .arrow-icon
        font-size :.24rem
  .home{
    font-size: 50px;
  }
</style>
