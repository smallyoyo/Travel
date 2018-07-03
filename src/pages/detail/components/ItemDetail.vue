<template>
  <div class="bg">
    <div class="out">
      <div class="item border-bottom">
        <h2 class="item-title">{{destine.tickeName}}</h2>
        <div class="item-close iconfont" @click="handlerClose">&#xe613;</div>
      </div>
      <div class="detail border-bottom">
        <div class="item-detail">
          <div class="item-header">
            <span class="title-icon">|</span>
            <span>预计说明</span>
          </div>
          <div class="destine">
            <div class="destine-time">预定时间：</div>
            <div class="destine-out">
              <div class="destine-mp">
                <span class="destine-content">{{destine.destineTime}}</span>
              </div>
              <p class="destine-desc">需要在游玩当天的17:30前预订</p>
            </div>
          </div>
          <div class="destine">
            <div class="destine-time">有 效 期：</div>
            <div class="destine-out">
              <p class="destine-desc">{{destine.validityPeriod}}</p>
            </div>
          </div>
        </div>
        <div class="item-detail">
          <div class="item-header">
            <span class="title-icon">|</span>
            <span>入园须知</span>
          </div>
          <div class="destine">
            <div class="destine-time">景区开发时间：</div>
            <div class="destine-out">
              <p class="destine-desc" v-html="destine.openTiem"></p>
            </div>
          </div>
        </div>
        <div class="item-detail">
          <div class="item-header">
            <span class="title-icon">|</span>
            <span>使用说明</span>
          </div>
          <div class="destine">
            <div class="destine-out">
              <p class="destine-desc line">
                夏各庄路口南太务收费站左转即可到达金海湖。
              </p>
            </div>
          </div>
        </div>
        <div class="item-detail">
          <div class="item-header">
            <span class="title-icon">|</span>
            <span>退款说明</span>
          </div>
          <div class="destine">
            <div class="destine-time">预定时间：</div>
            <div class="destine-out">
              <div class="destine-mp">
                <span class="destine-content">随时退</span>
              </div>
              <p class="destine-desc" v-html="destine.explanation"></p>
            </div>
          </div>
          <div class="destine">
            <div class="destine-time">极速处理：</div>
            <div class="destine-out">
              <p class="destine-desc">{{destine.rapidProcessing}}</p>
            </div>
          </div>
        </div>
        <div class="item-detail">
          <div class="item-header">
            <span class="title-icon">|</span>
            <span>费用说明</span>
          </div>
          <div class="destine">
            <div class="destine-out">
              <p class="destine-desc line" v-html="destine.expenseDescription"></p>
            </div>
          </div>
        </div>
      </div>
      <div class="pay">
        <div class="linePay">
          在线支付<span class="unit">¥<span class="price">83</span></span>
        </div>
        <div class="chat border-left">
          <div>
            <span class="iconfont">&#xe7dc;</span>
            咨询
          </div>
        </div>
        <div class="now">立即预定</div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: 'ItemDetail',
  props: {
    destine: Object
  },
  data () {
    return {
    }
  },
  methods: {
    handlerClose () {
      this.$emit('detailClose')
    }
  }
}
</script>
<style lang='stylus' scoped>
  .bg
    position: absolute
    top: 0
    height: 100%
    width: 100%
    background: rgba(0,0,0,.5)
    z-index: 10
    .out
      position: fixed
      bottom: 0
      z-index: 20
      background: #ffffff
      .item
        padding: 0 .7rem 0 .3rem
        line-height: 1.5rem
        height: 1.5rem
        position: relative
        .item-title
          font-size: .32rem
          font-weight: 700
          text-indent: .2rem
          color: #333
        .item-close
          position: absolute
          top: -0.3rem
          right: 0
          width: .88rem
          text-align: center
          font-size: .42rem
          color: #9e9e9e
      .detail
        height: 10rem
        background: #ffffff
        overflow-y: auto
        padding-bottom: 1rem
        .item-detail
          margin-top: .3rem
  .item-header
    padding: 0 .2rem
    line-height: .8rem
    font-size: .32rem
    font-weight: 500
    .title-icon
      color: #1ba9ba
      font-weight: 700
  .destine
    line-height: .4rem
    margin-top: .08rem
    .destine-time
      padding: 0 0 0 .4rem
      width: 1.4rem
      display: block
      float: left
    .destine-out
      overflow: hidden
  .destine-content
    background:  linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
    color: #ffffff
    padding: .08rem .1rem
    font-size: .25rem
  .destine-desc
    color: #616161
    word-break: break-all
    word-wrap: break-word
    font-size: .28rem
    overflow: hidden
    padding: 0 .1rem 0 .03rem
  .line
    padding: 0 .4rem 0 .4rem
  .pay
    width: 100%
    height: 1rem
    line-height: 1rem
    z-index: 40
    text-align: center
    position: absolute
    bottom: 0
    background: #ffffff
    color: #999
    .unit
      color: #ff9800
      font-size: .24rem
      padding-left: .15rem
      .price
        font-size: .48rem
    .linePay
      float: left
      width: 40%
      overflow: hidden
    .chat
      width: 20%
      float: left
      overflow: hidden
      .chat-icon
        font-size: .2rem
    .now
      float: left
      width: 40%
      overflow: hidden
      background: #ff9800
      color: #ffffff
      font-size: .4rem
</style>
