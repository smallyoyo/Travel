<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/85/85aa0c000578a01e90.water.jpg_200x200_0ccb4aa8.jpg',
        title: '细嗅历史的气息',
        desc: '阅尽沧桑，不变的是恬静，待君细细品味'
      },
      {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/6f/6fd1ba315b60e430a3.water.jpg_200x200_16184926.jpg',
        title: '寻魅力江南古镇',
        desc: '发呆静思，度过一个悠闲的下午'
      },
      {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/14/3dfad2bcd30c40e91a15f8b7296d86a6.jpg_200x200_265db173.jpg',
        title: '细嗅历史的气息',
        desc: '阅尽沧桑，不变的是恬静，待君细细品味'
      },
      {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/27/6640b07ce9a3dd7d9e37743ff58c1c3f.water.jpg_200x200_d7cd9982.jpg',
        title: '古典园林逛个够',
        desc: '如果是第一次来苏州，园林是一定要逛的'
      },
      {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/cd/cde718c195cc7cb0.water.jpg_200x200_30d44a00.jpg',
        title: '山清水秀之地',
        desc: '钟情于山水之间，别有一番雅致'
      },
      {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/cd/cde718c195cc7cb0.water.jpg_200x200_30d44a00.jpg',
        title: '细嗅历史的气息',
        desc: '阅尽沧桑，不变的是恬静，待君细细品味'
      },
      {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1802/80/80c0ccee0d2debf9a3.img.jpg_200x200_6ca992e6.jpg',
        title: '细嗅历史的气息',
        desc: '阅尽沧桑，不变的是恬静，待君细细品味'
      },
      {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/bcc9329d8af6f5cdddff715ed11a90fd.jpg_200x200_e5a812cd.jpg',
        title: '细嗅历史的气息',
        desc: '阅尽沧桑，不变的是恬静，待君细细品味'
      }]
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
