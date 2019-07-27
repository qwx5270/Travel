<template lang="html">
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img"  :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1564220482070&di=b7be2b69a7690f846f3754e49b0be8ef&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fblog%2F201508%2F17%2F20150817181059_Xw42t.jpeg'
      }, {
        id: '002',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1564223286176&di=c062e74e645062db0a1aa538bd4cdcb9&imgtype=0&src=http%3A%2F%2Fbaiducdn.pig66.com%2Fuploadfile%2F2017%2F0511%2F20170511114619713.jpg'
      }, {
        id: '003',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1564220482034&di=ec19025e7343bf1467912c3bee38fc44&imgtype=0&src=http%3A%2F%2Fpic.rmb.bdstatic.com%2Fb9983f233fb722d62d4f34a66ea2ba0d.jpeg'
      }, {
        id: '004',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1564220482034&di=b069aad02b5c933601282dc897354fd6&imgtype=0&src=http%3A%2F%2Fgss0.baidu.com%2F-fo3dSag_xI4khGko9WTAnF6hhy%2Flvpics%2Fh%3D800%2Fsign%3Dc1a206132f2dd42a40090cab333a5b2f%2Fb8389b504fc2d56293bd8397ed1190ef76c66c16.jpg'
      }, {
        id: '005',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1564220482069&di=b7bf342ee90d0305c78b4d52d8ad7622&imgtype=0&src=http%3A%2F%2Fimg2.3lian.com%2F2014%2Ff4%2F129%2Fd%2F49.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 62.5%
    background: #eee
  .swiper-img
    width: 100%
</style>
