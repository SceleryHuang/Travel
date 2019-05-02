<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src = "//img1.qunarzz.com/sight/p0/201403/03/77a8f60ea243465fdf2c937e2edd33dd.jpg_600x330_70c8f6d2.jpg" />
      <div class="banner-info">
        <div class="banner-title">国色天香水上乐园</div>
        <div class="banner-number">
          <span class="banner-icon">&#xe626;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_r_800x800_fa912897.jpg', 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_r_800x800_fa912897.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position :relative
    overflow: hidden
    height :0
    padding-bottom :55%
    text-align :left
    .banner-img
      width: 100%
    .banner-info
      display :flex
      position :absolute
      left: 0
      right:0
      bottom :0
      line-height :0.6rem
      color : #fff
      background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex:1
        font-size :.32rem
        padding :0 .2rem
      .banner-number
        margin-top :.14rem
        line-height :.4rem
        padding :0 .4rem
        height :.32rem
        border-radius :.2rem
        background :rgba(0,0,0,.8)
        font-size :.24rem
        .banner-icon
          font-size :.24rem
</style>
