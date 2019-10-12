<template>
  <div class="wapper">
    <swiper :options="swiperOption" v-if="swiperList.length!==0">
      <swiper-slide v-for="item of swiperList"
                    :item="item"
                    :key="item.id"  >
        <img class="swiper-img"  :src="item.imgUrl" alt />
      </swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
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
      }
    }
  },
  props: {
    swiperList: Array
  }
}
</script>

<style lang="stylus" scoped>
.wapper >>> .swiper-pagination-bullet-active {
  background: #fff !important;
}

.wapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 31.25%;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
