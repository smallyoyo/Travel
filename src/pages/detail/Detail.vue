<template>
  <div class="detail">
    <detail-banner :sightName="sightName" :bannerImg="bannerImg" :bannerImgs="gallaryImgs"></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list" @detailchange="handlerDetailShow"></detail-list>
      <detail-comment :commentList="commentList"></detail-comment>
      <detail-recommend :spotsList="spotsList"></detail-recommend>
    </div>
    <item-detail v-show="detailShow" :detailShow="detailShow" :destine="destine" @detailClose="detalClose"></item-detail>
  </div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailComment from './components/Comment'
import DetailRecommend from './components/Recommend'
import ItemDetail from './components/ItemDetail'
import axios from 'axios'
export default{
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
    DetailComment,
    DetailRecommend,
    ItemDetail
  },
  data () {
    return {
      sightName: '',
      bannerImg: '',
      gallaryImgs: [],
      list: [],
      commentList: [],
      spotsList: [],
      detailShow: false,
      destine: {}
    }
  },
  methods: {
    getDeatilInfo () {
      axios.get('/api/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.sightName = data.sightName
        this.bannerImg = data.bannerImg
        this.gallaryImgs = data.gallaryImgs
        this.list = data.categoryList
        this.commentList = data.commentList
        this.spotsList = data.spotsList
      }
    },
    handlerDetailShow (id) {
      if (!this.detailShow) {
        axios.get('/api/destine.json', {
          params: {
            id: id
          }
        }).then(this.handleGetDestineSuccess)
      }
      this.detailShow = !this.detailShow
    },
    handleGetDestineSuccess (res) {
      res = res.data
      if (res.ret && res.data) {
        const destineData = res.data
        this.destine = destineData
      }
    },
    detalClose () {
      this.detailShow = false
    }
  },
  mounted () {
    this.getDeatilInfo()
  }
}
</script>
<style lang="stylus" scoped>
  .detail
    position: relative
  .content
    height: 50rem
</style>
