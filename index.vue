<template>
  <swiper :options="swiperOptionh">
    <swiper-slide>
      <swiper :options="swiperOptionv">
        <swiper-slide>Vertical Slide 1</swiper-slide>
        <swiper-slide>Vertical Slide 2</swiper-slide>
        <swiper-slide>Vertical Slide 3</swiper-slide>
        <swiper-slide>Vertical Slide 4</swiper-slide>
        <swiper-slide>Vertical Slide 5</swiper-slide>
        <div class="swiper-pagination swiper-pagination-v" slot="pagination"></div>
      </swiper>
    </swiper-slide>
    <swiper-slide>Horizontal Slide 2</swiper-slide>
    <div class="swiper-pagination swiper-pagination-h" slot="pagination"></div>
  </swiper>
</template>

<script>
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
  export default {
    components: {
      swiper,
      swiperSlide
    },
    data() {
      return {
        swiperOptionh: {
          spaceBetween: 50,
          pagination: {
            el: '.swiper-pagination-h',
            clickable: true
          },
          loop: true,
          autoplay: {
            delay: 4000,
            disableOnInteraction: false
          },
        },
        swiperOptionv: {
          direction: 'vertical',
          spaceBetween: 50,
          pagination: {
            el: '.swiper-pagination-v',
            clickable: true
          },
          loop: true,

          autoplay: {
            delay: 1000,
            disableOnInteraction: false
          },
        }
      }
    }
  }
</script>

