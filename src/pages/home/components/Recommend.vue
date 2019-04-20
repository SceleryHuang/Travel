<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key = "item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name:'HomeRecommend',
    data () {
      return{
        recommendList:[{
          id: '0001',
          imgUrl:'http://img1.qunarzz.com/sight/p0/1807/ad/ad574bfe6c9e1ceda3.img.png_200x200_ea7a0734.png',
          title:'成都欢乐谷',
          desc:'超级过瘾过山车让你爽到怀疑人生'
        },{
          id: '0002',
          imgUrl:'http://img1.qunarzz.com/sight/p0/1809/1f/1f39774291457a42a3.img.jpg_200x200_e2d8001d.jpg',
          title:'石象湖',
          desc:'看花好去处'
        },{
          id: '0003',
          imgUrl:'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
          title:'成都海昌极地海洋公园',
          desc:'蠢萌蠢萌企鹅陪你爽翻这个春天'
        }
        ]
      }
    }
  }
</script>

<style lang = "stylus" scoped>
  @import "~styles/mixins.styl"
.title
  margin-top :.2rem
  line-height :.8rem
  background :#eee
  text-indent :.2rem
  ellipsis()
.item
  overflow :hidden
  display :flex
  height :1.9rem
  .item-img
    width :1.7rem
    height :1.7rem
    padding :.1rem
  .item-info
    text-align :left
    flex :1
    padding :.1rem
    min-width :0
    .item-title
      line-height :.54rem
      font-size :.32rem
      ellipsis()
    .item-desc
      color :#cccccc
      line-height :.4rem
      ellipsis()
    .item-button
      background :#ff9300
      padding :0 .2rem
      border-radius : .6rem
      margin-top :.2rem
      color:#fff
      line-height :.4rem

</style>
