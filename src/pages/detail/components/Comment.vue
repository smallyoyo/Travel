<template>
  <div>
    <div class="comment-title border-bottom">
      <span class="title-icnon">|</span>
      用户评论
    </div>
    <div class="comment" v-for="item of commentList" :key="item.id">
      <div class="comment-header">
        <div class="star iconfont">
          <span v-for="(star,index) of item.star" :key="index">&#xe6b0;</span>
        </div>
        <div class="time">{{item.nickName}}  {{item.uploadDate}}</div>
      </div>
      <div class="comment-content">
        {{item.comment}}
      </div>
      <div class="comment-imgs">
        <div class="comment-imgout" v-for="(img,index) of item.commentImg" :key="index" @click="handlerBannerClick">
          <div class="comment-imginner">
            <img class="comment-img" :src="img"/>
          </div>
        </div>
      </div>
      <div class="img-count">
          共{{item.commentImg.length}}张
      </div>
      <fade-animation>
        <common-gallary :imgs="item.commentImg" v-show="showGallary" @close="handlerGallaryClose"></common-gallary>
      </fade-animation>
    </div>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default{
  name: 'DetailComment',
  props: {
    commentList: Array
  },
  data () {
    return {
      showGallary: false
    }
  },
  methods: {
    handlerGallaryClose () {
      this.showGallary = false
    },
    handlerBannerClick () {
      this.showGallary = true
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  }
}
</script>
<style lang="stylus" scoped>
  .comment
    position: relative
  .comment-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
    .title-icnon
      color: #1ba9ba
      font-weight: 700
  .comment-title,.comment
    padding: 0 .2rem
  .comment-header
    line-height: .8rem
    height: .8rem
    .star
      float: left
      color: orange
      font-size: .24rem
    .time
      float: right
  .comment-content
    line-height: .42rem
    font-size: .26rem
    color: #616161
  .comment-imgs
    margin: .02rem 0 .02rem 0
    overflow: hidden
    .comment-imgout
      float: left
      width: 33.3%
      margin-bottom: .1rem
      .comment-imginner
        margin-left: .07rem
        margin-right: .07rem
        padding-bottom: 70%
        height: 0
        .comment-img
          width: 100%
          background: url(https://s.qunarzz.com/piao_topic/image/common/default/140x140.png)
          background-size: contain
  .img-count
    position: absolute
    right: .27rem
    bottom: .5rem
    height: .5rem
    width: .94rem
    line-height: .5rem
    border-top-left-radius: .2rem
    border-bottom-left-radius: .2rem
    background: #000
    color: #fff
    opacity: .5
</style>
