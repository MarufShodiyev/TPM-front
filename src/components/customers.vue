<template>
    <div class="customer">
        <div class="container">
            <div class="customer_wrapper">
                <Title class="center" title="Testimonials" />
                <PageInfo class="center"
                    title="Lorem ipsum dolor sit amet consectetur. Metus eget risus viverra malesuada faucibus nulla at viverra. Eget ac elementum vel nunc non tempor. Nec dignissim massa elementum eu venenatis lorem. Viverra integer nibh tellus morbi sed." />

                <swiper :modules="modules" :slides-per-view="3" :space-between="32" navigation 
                    :pagination="{ clickable: true }" @swiper="onSwiper" @slideChange="onSlideChange">
                    <swiper-slide v-for="(item, index) in customer" :key="index">
                        <ul>
                            <li>
                                <p>
                                    {{ item.title }}
                                </p>
                                <div class="customer__comma">
                                    <div class="customer_img">
                                        <div>
                                            <img :src="item.image" alt="customer.png">
                                        </div>
                                        <h5>{{ item.name }}</h5>
                                    </div>
                                    <div class="comma_img">
                                        <img :src="item.comma" alt="comma img ">
                                    </div>
                                </div>
                            </li>
                        </ul>
                        <div class="swiper-pagination"></div>
                    </swiper-slide>
                </swiper>
            </div>
        </div>

    </div>
</template>

<script setup>
import Title from './ui/title.vue'
import PageInfo from './ui/pageinfo.vue'
import { reactive, ref } from 'vue';
import img from "@/assets/images/customer.png"
import commaimg from '@/assets/icons/comma_icon.svg'


// import Swiper core and required modules
import { Pagination } from 'swiper/modules';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/pagination';

const customer = reactive([
    {
        title: "Customer support deserves special mention. The TPM team is not only responsive but also proactive in addressing any concerns. Their commitment to resolving issues promptly reflects a level of professionalism that is truly commendable.",
        image: img,
        name: "Xurshid Istamov",
        comma:commaimg
    },
    {
        title: "Customer support deserves special mention. The TPM team is not only responsive but also proactive in addressing any concerns. Their commitment to resolving issues promptly reflects a level of professionalism that is truly commendable.",
        image: img,
        name: "Xurshid Istamov",
        comma:commaimg
    },
    {
        title: "Customer support deserves special mention. The TPM team is not only responsive but also proactive in addressing any concerns. Their commitment to resolving issues promptly reflects a level of professionalism that is truly commendable.",
        image: img,
        name: "Xurshid Istamov",
        comma:commaimg
    },
    {
        title: "Customer support deserves special mention. The TPM team is not only responsive but also proactive in addressing any concerns. Their commitment to resolving issues promptly reflects a level of professionalism that is truly commendable.",
        image: img,
        name: "Xurshid Istamov",
        comma:commaimg
    },
    {
        title: "Customer support deserves special mention. The TPM team is not only responsive but also proactive in addressing any concerns. Their commitment to resolving issues promptly reflects a level of professionalism that is truly commendable.",
        image: img,
        name: "Xurshid Istamov",
        comma:commaimg
    },


])

// Import Swiper styles
// export default {
//     components: {
//         Swiper,
//         SwiperSlide,
//     },
//     setup() {

//         return {
//             onSwiper,
//             onSlideChange,
//             modules: [Pagination],
//         };
//     },
// };

// const onSwiper = (swiper) => {
//     console.log(swiper);
// };
// const onSlideChange = () => {
//     console.log('slide change');
// };

const modules = ref([Pagination])
</script>



<style scoped>
.swiper-pagination{
    padding: 50px 0px;
}
.customer {
    background: linear-gradient(180deg, #FFF 0%, #F6F9FF 100%);
}

.customer_wrapper {
    margin-top: 120px;
}

.center {
    text-align: center;
    margin: 0px auto;
}

ul {
    margin-top: 68px;
    display: flex;
    align-items: center;
    flex-wrap: nowrap;
    padding-bottom: 100px;
}

.swiper-pagination {
    padding-bottom: 250px;
}

ul li {
    max-width: 500px;
    padding: 24px 32px;
    border-radius: 10px;
    background: var(--black-white-white, #FFF);
}

ul li p {
    color: var(--system-colors-gray-800, #1C232C);
    font-size: 16px;
    font-weight: 500;
    line-height: 32px;
}
.customer__comma{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.customer_img {
    margin-top: 20px;
    display: flex;
    align-items: center;
    gap: 17px;
}

.customer_img div img {
    border-radius: 48px;
    border: 2px solid var(--additional-colors-indigo-500, #6265F0);
    background: var(--avatars-square-image-13-john-moccy, url(<path-to-image>), lightgray 50% / cover no-repeat, #D4D3D3);
}
</style>