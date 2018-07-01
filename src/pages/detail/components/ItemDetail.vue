<template>
  <div class="bg" v-if="showDetail">
    <div class="out">
      <div class="item border-bottom">
        <h2 class="item-title">大连圣亚海洋世界(AAAA景区)</h2>
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
                <span class="destine-content">17:30前随买随用</span>
              </div>
              <p class="destine-desc">需要在游玩当天的17:30前预订</p>
            </div>
          </div>
          <div class="destine">
            <div class="destine-time">有 效 期：</div>
            <div class="destine-out">
              <p class="destine-desc">游玩日期当天有效</p>
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
              <p class="destine-desc">
                周一～周五：08:30～16:30开放；<br/>
                周一～周五：08:30～16:30开放；
              </p>
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
                费用包含
                <br>
                【散客自驾】金海湖风景区成人门票+快艇票，节假日通用！
                <br>
                使用方法
                <br>
                入园方式：凭【大方向票务】短信电子码验证入园
                <br>
                入园时间：8:30-16:00 以景区为主
                <br>
                入园地址：金海湖景区西门游客中心
                <br>
                退款说明
                <br>
                随时退，未消费(包含过期)的旅游商品支持随时申请退款
                <br>
                其他说明
                <br>
                儿童价：身高1.2米以下免费
                <br>
                老年票：老年证半价，北京市老年优待卡免票
                <br>
                其他（如军官证、教师优惠等）军官证、学生证半价；记者证、离休证、残疾证免票
                <br>
                地址路线
                <br>
                公交路线
                <br>
                东直门乘918路至平谷可达。
                <br>
                自驾路线
                <br>
                走京平高速，到夏各庄路口南太务收费站左转即可到达金海湖。
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
              <p class="destine-desc">90天内支持随时退款，经核实如未取票，可免费取消
              </p>
            </div>
          </div>
          <div class="destine">
            <div class="destine-time">极速处理：</div>
            <div class="destine-out">
              <p class="destine-desc">去哪儿网承诺，提交申请后一个工作日内完成退款申请的审核
              </p>
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
              <p class="destine-desc line">
                金海湖风景区成人门票+快艇票<br/>
                6月3日10点以后开始验票<br/>
                <br/>
              </p>
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
  name: "ItemDetail",
  data () {
    return {
      showDetail: true
    }
  },
  methods: {
    handlerClose () {
      this.showDetail = !this.showDetail
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