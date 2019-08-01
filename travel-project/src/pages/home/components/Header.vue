<template lang="html">
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe615;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  /* 1rem = html font-size = 50px */
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .32rem
    .header-input
      flex: 1
      background: #fff2
      height: .64rem
      line-height: .64rem
      border-radius: .1rem
      margin-left: .2rem
      margin-top: .12rem
      padding-left: .2rem
      color: #ccc
    .header-right
      min-width: 1.05rem
      padding: 0 .1rem
      float: rigth
      text-align: center
      color: #fff
      .arrow-icon
        font-size: .25rem
        margin-left: .06rem
</style>
