<template lang="html">
  <div class="">
    <div class="recommend-title">
      热销推荐
    </div>
    <ul>
      <router-link tag="li" class="item border-bottom" v-for="item of list"
                   :key="item.id" :to="'/detail/' + item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
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
    margin-top: .15rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.8rem
      height: 1.8rem
      padding: .13rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .55rem
        font-size: .35rem
        ellipsis()
      .item-desc
        line-height: .45rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .18rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
