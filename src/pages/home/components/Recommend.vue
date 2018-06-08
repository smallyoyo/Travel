<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background:#eee
    /**
     * text-indent
     * 首行缩进
     * @type {[css]}
     */
    text-indent: .2rem
  .item
    overflow:hidden
    display:flex
    height:2.4rem
    .item-img
      width:2rem
      height:2rem
      padding: .2rem
    .item-info
      flex:1
      padding: .2rem
      min-width:0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height: .44rem
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
        margin-top: .2rem
        color:#fff
</style>
