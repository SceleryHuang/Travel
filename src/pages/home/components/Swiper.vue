<template>
  <div class="wapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for = 'item of swiperList' :key="item.id">
      <img class="swiper-img" :src="item.imgUrl"/>
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop:true
      },
      swiperList: [ {
        id: '0001',
        imgUrl :'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/26c9b54e3e02d3724f614883d77a62c6.jpg_750x200_57aa8efa.jpg'
      }, {
        id: '0002',
        imgUrl :'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/88be3fcb5a2e55f7a99d6f372e54ee1a.jpg_750x200_c6561823.jpg'
      }, {
        id: '0003',
        imgUrl :'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/437a486a1627adae39ab30e4d98fbcee.jpg_750x200_d8477149.jpg'
      }]
    }
   }
}
</script>

<style lang="stylus" scoped>
  /*样式穿透*/
  .wapper >>> .swiper-pagination-bullet-active
    background :#fff !important
  .wapper
    width: 100%
    overflow:hidden
    height:0
    padding-bottom:26.5%
    /*height :31.25vm*/
    .swiper-img
      width:100%
</style>
