<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont icon-fanhui"></span>
    </div>
    <div class="header-input">
      <span class="iconfont icon-sousuo"></span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.$store.state.city}}
        <span class="iconfont icon-jiantou arrow-icon"></span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  // @import '~@/assets/styles/variables.styl'
  @import '~styles/variables.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    .header-left
      width: .64rem
      float: left
      text-align: center
    .header-input
      flex: 1
      height: .64rem
      line-height .64rem
      margin-top: .12rem
      margin-left: .6rem
      padding-left: .2rem
      background: #ffffff
      border-radius: .1rem
      color: #ccc
    .header-right
      min-width 1.24rem
      padding: .1rem
      float: right
      text-align: center
      color: #ffffff
      .arrow-icon
        margin-left: -0.04rem
        font-size: .24rem
</style>
