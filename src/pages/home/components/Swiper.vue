<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
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
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts3/1806/3d/334a32508135002.jpg_r_390x260x90_dc044bb6.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1806/10/4315c52d21915b02.jpg_r_390x260x90_bd3c92da.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper>>>.swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow:hidden
    width: 100%
    height:0
    padding-bottom: 66.67%
    background: #eee
    .swiper-img
      width: 100%
</style>
