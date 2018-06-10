<template>
  <div>
    <div class="banner" @click="handlerBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1603/85/85aa0c000578a01e90.water.jpg_600x330_6dddcf68.jpg">
      <div class="banner-info">
        <div class="banner-title">
          拙政园(AAAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe626;</span>
          68
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handlerGallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default{
  name: 'DetailBanner',
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1707/69/6955be3eda826b3a3.img.png_r_800x800_8fdcde1d.png',
        'http://img1.qunarzz.com/sight/p0/1707/a5/a5b2d37085f6f03fa3.img.png_r_800x800_51c4f101.png'],
      showGallary: false
    }
  },
  methods: {
    handlerBannerClick () {
      this.showGallary = true
    },
    handlerGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
     width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        padding: 0 .4rem
        margin-top: .14rem
        line-height: .32rem
        border-radius: .2rem
        font-size: .24rem
        background: rgba(0, 0, 0, .8)
        .banner-icon
          font-size: .24rem
</style>
