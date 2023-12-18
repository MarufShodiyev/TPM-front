<template>
 <div class="container temp">
  <swiper
    :modules="modules"
    :slides-per-view="3"
    :space-between="100"
    navigation
    :pagination="{ clickable: true }"
  
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide id="top">Slide 1</swiper-slide>
    <swiper-slide>Slide 2</swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide>
    <swiper-slide>Slide 5</swiper-slide>
    <swiper-slide>Slide 6</swiper-slide>
    <swiper-slide>Slide 7</swiper-slide>
  </swiper>
 </div>
</template>
<script>
  // import Swiper core and required modules
  import {Pagination } from 'swiper/modules';

  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/pagination';
  // import 'swiper/css/navigation';
  // import 'swiper/css/scrollbar';

  // Import Swiper styles
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [ Pagination],
      };
    },
  };
</script>

<style scoped>
  .temp{
    padding:50px 0px 40px;
    height: 60px;
    text-align: center;
  }
  #top{
    margin-top: 30px;
  }
 
</style>