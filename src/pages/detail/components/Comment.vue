<template>
  <div>
    <div class="comment-title border-bottom">
      <span class="title-icnon">|</span>
      用户评论
    </div>
    <div class="comment">
      <div class="comment-header">
        <div class="star iconfont">&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;</div>
        <div class="time">j*8  2018-06-04</div>
      </div>
      <div class="comment-content">
        {{comment}}
      </div>
      <div class="comment-imgs">
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/5c/5b87ef806c352402.jpg_228x168_4c068a2a.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://img1.qunarzz.com/sight/p0/1603/85/85aa0c000578a01e90.water.jpg_600x330_6dddcf68.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
      </div>
    </div>
        <div class="comment">
      <div class="comment-header">
        <div class="star iconfont">&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;</div>
        <div class="time">j*8  2018-06-04</div>
      </div>
      <div class="comment-content">
        {{comment}}
      </div>
      <div class="comment-imgs">
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/5c/5b87ef806c352402.jpg_228x168_4c068a2a.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://img1.qunarzz.com/sight/p0/1603/85/85aa0c000578a01e90.water.jpg_600x330_6dddcf68.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
        <div class="comment-imgout">
          <div class="comment-imginner">
            <img class="comment-img" src="https://imgs.qunarzz.com/piao/fusion/1806/c5/745c1d3b4136fe02.jpg_228x168_98ba7a63.jpg"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: 'DetailComment',
  data () {
    return {
      comment: '今天是个好天气，当然也有好心情啦，第一次来苏州，苏州给我的第一印象是古风古韵的城市，干净清爽。就连公交站亭和WC都那充满了诗情画意，让人感觉是来到了一个文雅的城市， 无形中提高了个人的道德与修养。城市在这个季节绿意昂然，生机勃勃。为整个城市的格局加分不少，不愧有“上有天堂，下有苏杭"的美誉。城市地标东方之门配合苏州中心，大手笔高格局，美！美！美！(晚上更适合去哟，苏州中心的玻璃幕墙的瀑布设计尤为出彩，更具高大上)最为重要的是美女也很多哟，高颜值，皮肤好，身材棒！'
    }
  }
}
</script>
<style lang="stylus" scoped>
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
</style>