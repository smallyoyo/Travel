<template>
  <div>
    <div class="recommend-header border-bottom">
      <span class="header-icon">|</span>
      看了该景点的人还看了
    </div>
    <div>
      <div class="spots" v-for="item of spotsList" :key="item.id">
        <div class="spots-img">
          <img class="img" :src="item.spotsImg">
        </div>
        <div class="spots-info border-bottom">
          <div class="spots-name">
            {{item.spotsNmae}}<span class="spots-price">¥{{item.price}}<span class="qi">起</span></span>
          </div>
          <div class="spots-other">
            <div class="star iconfont">
              <span class="stars">&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;</span>
              <span class="comment">{{item.commentCount}}条评论</span>
            </div>
            <div class="address">{{item.address}}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: 'DetailRecommend',
  props: {
    spotsList: Array
  }
}
</script>
<style lang="stylus" scoped>
  .recommend-header
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
    .header-icon
      color: #1ba9ba
      font-weight: 700
  .spots
    overflow: hidden
    padding: .2rem 0 .2rem .2rem
    display: flex
    flex-direction: row
    justify-content: flex-start
    flex-wrap: nowrap
    .spots-img
      width: 27%
      overflow: hidden
      .img
        width: 1.68rem
        height: 1.68rem
        object-fit: cover
    .spots-info
      line-height: .4rem
      width: 73%
      position: relative
      .spots-name
        font-size: .3rem
        color: #212121
        .spots-price
          color: #ff9800
          position: absolute
          right: .2rem
          font-size: .35rem
          .qi
            color: #9e9e9e
            font-size: .2rem
      .spots-other
        position: absolute
        bottom: .1rem
        .star
          color: #9e9e9e
          font-size: .25rem
          .stars
            color: #ffb436
          .comment
            padding-left: .2rem
        .address
          color: #9e9e9e
          font-size: .25rem
</style>
