
  <!-- The ref attr used to find the swiper instance -->
  <template>
    <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl" ></swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </template>
<script>
export default{
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList:
        [{
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/54862f4b1501e202.jpg_640x200_886ddf82.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/1b/6c766b79e2045102.jpg_640x200_3e44c74a.jpg'
        }]
    }
  }
}
</script>
<style scoped lang="stylus">
.wrapper >>> .swiper-pagination-bullet-active
  background:#fff
.wrapper
  overflow:hidden
  width:100%
  height:0
  padding-bottom:31.25%
  background:#eee
  .swiper-img
    width:100%
</style>
