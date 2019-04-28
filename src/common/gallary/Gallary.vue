<template>
  <div class="container">
    <div class="wapper">
      <swiper :options="swiperOption" v-if = "showSwiper">
      <!-- slides -->
      <swiper-slide v-for = 'item of list' :key="item.id">
        <img class="gallary-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  data(){
    return{
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container
    display :flex
    flex-direction :column
    justify-content :center
    z-index: 99
    position: fixed
    left :0
    right :0
    top: 0
    bottom:0
    background :#000
    .wapper
      width :100%
      height :0
      overflow : hidden
      padding-bottom :100%
      .gallary-img
        width :100%
</style>
