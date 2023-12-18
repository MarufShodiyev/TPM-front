<template>
    <div class="partners" id="partners">
      <div class="container">
        <div class="partners-wrapper">
          
          <Carousel :settings="settings.settings" :breakpoints="settings.breakpoints" :wrap-around="true" :transition="5000"  :autoplay="Infinity">
            <Slide v-for="slide in 20" :key="slide">
              <div class="carousel__item">
                 <img src="src/assets/images/partners2.png" alt="">
              </div>
            </Slide>
          </Carousel>
  
          <Carousel style="margin: 30px 0;" :settings="settings.settings" :breakpoints="settings.breakpoints" :wrap-around="true" :transition="3000"  dir="rtl" :autoplay="Infinity">
            <Slide v-for="slide in 20" :key="slide">
              <div class="carousel__item">
                 <img src="src/assets/images/partners1.png" alt="">
              </div>
            </Slide>
          </Carousel>
          
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { reactive } from 'vue'
  import { Carousel,  Slide } from 'vue3-carousel'
  
  import 'vue3-carousel/dist/carousel.css'
  
  const settings = reactive({
    settings: {
      itemsToShow: 4,
      snapAlign: "center"
     },
     breakpoints: {
      700: {
       itemsToShow: 2.5,
       snapAlign: "center"
      },
      1024: {
       itemsToShow: 3,
       snapAlign: "center"
      },
          1400:{
            itemsToShow: 4,
       snapAlign: "center"
          }
     }
  })
  </script>