<template>
  <div class="wapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList"
                    :item="item"
                    :key="item.id">
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
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/4950dc04db88330968906bc610caa524.jpg_750x200_1ee2ba8a.jpg'
        },
        {
          id: '0002',
          imgUrl:
            'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/78b240572657a6da67e662540c846dd6.jpg_750x200_b75c8be9.jpg'
        },
        {
          id: '0003',
          imgUrl:
            'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/c36914f22fdb82d2b8878cbf6dddac98.jpg_750x200_4a63da4b.jpg'
        }
      ]
    }
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
  padding-bottom: 27.25%;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
