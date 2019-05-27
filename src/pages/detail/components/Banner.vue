<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1502/15/15ca1d0eab6bf46c.water.jpg_600x330_1108fbd3.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          东部华侨城大侠谷
        </div>
        <div class="banner-number">
          <span class="iconfont icon-tupian banner-icon"></span>
          <span>19</span>
        </div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallary" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'

export default {
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1502/91/91b45435e2150822.water.jpg_r_800x800_aaa13bbf.jpg', 'http://img1.qunarzz.com/sight/p0/1502/fe/fe19db77df7adf49.water.jpg_r_800x800_57fa6a66.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGalleryClose () {
      this.showGallary = false
    }
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
      right: 0
      bottom: 0
      left: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex: 1
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        .banner-icon
          font-size: .24rem
</style>
