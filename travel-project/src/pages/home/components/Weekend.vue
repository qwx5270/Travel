<template lang="html">
  <div class="">
    <div class="recommend-title">
      周末去哪儿
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .recommend-title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    padding-bottom: 37.09%
    height: 0
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .55rem
      font-size: .33rem
      ellipsis()
    .item-desc
      line-height: .45rem
      color: #ccc
      ellipsis()
</style>
