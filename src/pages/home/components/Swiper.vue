<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
      	<img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>

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
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
      },{
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/9e/f625886dec6c0402.jpg_750x200_417be630.jpg'
      },{
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/13/e1188b0d0f21b902.jpg_750x200_f85c782a.jpg'
      }]
		}
	}
}
</script>
<style lang="stylus" scoped>
   // 穿透
  .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 27.78%
    background: #eee
    .swiper-img
	    width: 100%

</style>