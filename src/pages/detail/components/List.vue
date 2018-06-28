<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div class="item-content border-bottom" v-for="(contentItem,index) of item.contentList" :key="index">
        <div class="content-title">
          {{contentItem.content}}
        </div>
        <div class="item-price">
          ¥
          <em class="price">{{contentItem.price}}</em>
          <span class="qi">起</span>
          <span class="iconfont down">&#xe62d;</span>
        </div>
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
  .item-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
    .item-title-icon
      position: relative
      left: .06rem
      top: .09rem
      display: inline-block
      width: .36rem
      height: .36rem
      background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
      margin-right: .1rem
      background-size: .4rem 3rem
  .item-children
    padding: 0 .2rem
  .item-content
    line-height: .82rem
    font-size: .30rem
    padding: 0 .2rem
    display: flex
    flex-direction: row
    flex-wrap: nowrap
    justify-content: space-between
    .item-price
      color: #ff9800
      font-size: .24rem
      .price
        font-size: .42rem
      .qi
        font-size: .20rem
        color: #9e9e9e
      .down
        color: #9e9e9e
        font-size: .30rem
</style>
