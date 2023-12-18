<template>
    <div id="partners">
        <div class="container">
            <div class="partners_wrapper">
                <Title class="center" title="Our partners" />

                <div class="carousels">
                  <Carousel class="carousel" :settings="settings.settings" :breakpoints="settings.breakpoints"
                        :wrap-around="true" :transition="5000" :autoplay="Infinity">
                        <Slide v-for="(item, index) in partners" :key="index">
                            <div class="carousel__item">
                             
                                <img :src="item.image" alt="rasm bor">
                            </div>
                        </Slide>
                    </Carousel>
                      
                    <Carousel class="carousel" :settings="settings.settings" :breakpoints="settings.breakpoints"
                        :wrap-around="true" :transition="6000" dir="rtl" :autoplay="Infinity">
                        <Slide v-for="(item, index) in partners" :key="index">
                            <div class="carousel__item">
                                <img :src="item.image" alt="rasm bor">
                            </div>
                        </Slide>
                    </Carousel>
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
import Title from './ui/title.vue'
import { reactive } from 'vue';
import { Carousel,Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

import img1 from '../assets/images/partners1.png'
import img2 from '../assets/images/partners2.png'
import img3 from '../assets/images/partners3.png'

const partners = reactive([
    {
        image: img1
    },
    {
        image: img2
    },
    {
        image: img2
    },
    {
        image: img3
    },
    {
        image: img1
    },
    {
        image: img2
    },
    {
        image: img1
    },
    {
        image: img3
    },
    {
        image: img1
    }, {
        image: img3
    }, {
        image: img1
    }, {
        image: img2
    }, {
        image: img3
    }, {
        image: img1
    }, {
        image: img2
    }
])
console.log(partners)
const settings = reactive({
    settings: {
        itemsToShow: 4,
        snapAlign: "center"
    },
    breakpoints: {
        700: {
            itemsToShow: 2,
            snapAlign: "center"
        },
        1024: {
            itemsToShow: 2.5,
            snapAlign: "center"
        },
        1400: {
            itemsToShow: 3.5,
            snapAlign: "center"
        }
    }
})
</script>

<style scoped>
#partners {
    background: #FFF;
}

.partners_wrapper {
    margin-top: 52px;
    padding-bottom: 70px;
}

.center {
    margin: 0px auto;
    text-align: center;
}

.carousels {
    padding: 45px;
}

.carousel {
    padding-bottom: 30px;
}

.carousel__item {
    height: 120px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0px 25px;
    border-radius: 10px;
    border: 1px solid var(--system-colors-gray-200, #E0E3E6);
    opacity: 0.4;
    background: var(--black-white-white, #FFF);
}

</style>


