<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div class="item-content border-bottom" v-for="(contentItem,index) of item.contentList" :key="index" >
        <div class="content" @click="showDetailClick(index)">
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
        <div class="item-detail" v-for="detail of contentItem.detail" :key="detail.id" v-show="showDetail">
          <div class="detail border-bottom" @click="handlerShow(detail.id)">
            <div class="detail-content">
              <div class="detail-title">{{detail.title}}</div>
              <div class="detail-day">
                <span>
                  <img class="detail-day-img" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" />
                  <span>{{detail.time}}</span>
                </span>
              </div>
              <div class="detail-condition">
                <span class="return" v-for="(condition,index) of detail.condition" :key="index" v-html="condition"></span>
              </div>
            </div>
            <div class="detail-price">
              <div class="item-price">
                ¥
                <em class="price">{{detail.price}}</em>
              </div>
              <div class="detail-btn">
                <em>预订</em>
              </div>
            </div>
          </div>
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
  },
  data () {
    return {
      showDetail: false
    }
  },
  methods: {
    showDetailClick (index) {
      this.showDetail = !this.showDetail
    },
    handlerShow (id) {
      this.$emit('detailchange', id)
    }
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
    overflow: hidden
  .content
    padding: 0 .2rem
    line-height: .82rem
    font-size: .30rem
  .content-title
    float: left
    overflow: hidden
    width: 80%
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
  .item-detail
    background: #f5f5f5
    padding: 0 0
    .detail
      display: flex
      flex-direction: row
      flex-wrap: nowrap
      justify-content: space-between
      align-items: center
      padding: 0.2rem .2rem
      overflow: hidden
      .detail-content
        width: 76%
        color: #616161
        .detail-title
          line-height: .45rem
        .detail-day
          font-size: .23rem
          .detail-day-img
            width: .23rem
            height: .23rem
      .detail-price
        width: 24%
        text-align: center
        padding: 0 0 0 0.2rem
        .detail-btn
          height: .6rem
          line-height: .6rem
          background: linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%);
          border-radius: .1rem
          color: #ffffff
      .detail-condition
        margin: 0.16rem 0;
        .return
          color: #00afc7
          border: 1px solid #a5e4ec
          font-size: .2rem
          margin: 0 .03rem
      .show-detail,.jianright
        font-size: .24rem
</style>
