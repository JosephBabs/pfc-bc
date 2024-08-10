<template>
    <swiper :options="swiperOptions">
      <swiper-slide v-for="image in images" :key="image">
        <img :src="image" alt="Slide image">
      </swiper-slide>
    </swiper>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from 'swiper/swiper-vue.cjs.js';
  import 'swiper/swiper-bundle.css';
  
  export default {
    components: {
        Swiper,
    SwiperSlide
    },
    data() {
      return {
        images: [
          "/assets/images/slide/slider11.jpeg",
          '/assets/images/slide/slider12.jpeg',
          // Additional images
        ],
        swiperOptions: {
          loop: true,
          autoplay: {
            delay: 2500,
            disableOnInteraction: false,
          },
          pagination: {
            el: '.swiper-pagination',
            clickable: true,
          },
          navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev',
          },
        }
      };
    }
  };
  </script>
  
  <style>
  /* CSS here */
  </style>
  