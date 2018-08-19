<template>
  <div class="wrapper">
  <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img  class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
    export default {
        name: "HomeSwiper",
        data() {
          return{
            swiperOption:{
              pagination:'.swiper-pagination',
              loop:true
             /* paginationClickable: true,
              speed: 2000,
              observer:true,
              observeParents:true,
              autoplayDisableOnInteraction : false,
              autoplay:1500*/
            },
            swiperList:[{
              id:'0001',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/40/1d7be74ed1584002.jpg_750x200_c41233c9.jpg'
            },{
              id:'0002',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/bd/8e4a1c3f470d3702.jpg_750x200_f1f0a8c7.jpg'
            }]
          }
        }
    }
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
    .wrapper
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom:26.6%
      background :#333333
      .swiper-img
          width :100%
</style>
