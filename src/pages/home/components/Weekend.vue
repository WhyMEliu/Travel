<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-into">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeWenkend",
    data(){
      return {
        recommendList:[{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg",
          title:"寻找北京的皇城范儿",
          desc:"数百年的宫廷庙宇，至今依旧威严霸气"
        },
          {
            id:"0002",
            imgUrl:"http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg",
            title:"寻找北京的皇城范儿",
            desc:"数百年的宫廷庙宇，至今依旧威严霸气"
          },
          {
            id:"0003",
            imgUrl:"http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg",
            title:"寻找北京的皇城范儿",
            desc:"数百年的宫廷庙宇，至今依旧威严霸气"
          }]
      }
    }
  }
</script>
<style lang="stylus" scoped>
  @import "~@/assets/styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow :hidden
    height :0
    padding-bottom : 33.4%
  .item-img
    width : 100%
  .item-into
    padding : .1rem
    .item-title
      line-height : .54rem
      font-size : .32rem
      ellipsis()
    .item-desc
      line-height :.4rem
      color : #ccc
      ellipsis()
</style>
