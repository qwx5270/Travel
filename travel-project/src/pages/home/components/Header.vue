<template lang="html">
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe615;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  /* 1rem = html font-size = 50px */
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
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
      width: 1.25rem
      float: rigth
      text-align: center
      .arrow-icon
        font-size: .25rem
        margin-left: .06rem
</style>
