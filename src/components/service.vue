<template>
    <div id="services">
        <div class="container">
            <div class="service_wrapper">
                <Title class="center" title="Our services" />
                <PageInfo class="center page_info"
                    title="Lorem ipsum dolor sit amet consectetur. Metus eget risus viverra malesuada faucibus nulla at viverra. Eget ac elementum vel nunc non tempor. Nec dignissim massa elementum eu venenatis lorem. Viverra integer nibh tellus morbi sed." />
                <ul>
                    <li v-for="(item, index) in ser" :key="index">
                        <div>
                            <img :src="item.image">
                        </div>
                        <h3>{{ item.title }}</h3>
                        <p>
                            {{ item.info }}
                        </p>
                    </li>

                </ul>
            </div>
        </div>
    </div>
</template>
<script setup>
import Title from './ui/title.vue';
import PageInfo from './ui/pageInfo.vue';

import { reactive } from 'vue';

import img1 from "@/assets/images/parcel_menegment.svg"
import img2 from "@/assets/images/key_management.svg"
import img3 from "@/assets/images/booking_management.svg"
import img4 from "@/assets/images/technical_support.svg"



const ser = reactive([
    {
        image: img1,
        title: "Parcel Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img2,
        title: "Key Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    }, {
        image: img3,
        title: "Booking Managament",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img4,
        title: "Technical Support",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img1,
        title: "Parcel Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img1,
        title: "Parcel Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img1,
        title: "Parcel Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    },
    {
        image: img1,
        title: "Parcel Management",
        info: "Overall, parcel management aims to enhance the reliability, speed, and security of the parcel delivery process, contributing to a positive experience for both senders and recipients."

    }
])




</script>

<style  scoped>
#services {
    /* position: relative; */
    background: linear-gradient(180deg, #FFF 0%, #F6F9FF 100%);
    /* z-index: 1; */
}

.service_wrapper {
    margin-top: 100px;
   
}
/* 
#services::before {
    content: '';
    position: absolute;
    width: 600px;
    height: 600px;
    flex-shrink: 0;
    border-radius: 500px;
   
    background: rgba(226, 41, 0, 0.03);
    filter: blur(10px);
    left: -20%;
    top: -10%;
} */

.center {
    text-align: center;
    margin: 0px auto;
}

.page_info {
    margin-top: 21px;
}

ul {
    margin-top: 35px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 30px;
}

ul li {

    padding: 24px;
    max-width: 300px;
    border-radius: 10px;
    border: 1px solid var(--system-colors-gray-50, #F7F7F8);
    background: var(--black-white-white, #FFF);
    margin-bottom: 50px;
}


ul li div {
    border-radius: 10px;
    background: var(--additional-colors-indigo-50, #EEF2FF);
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 100px;
}

ul li h3 {
    margin-top: 16px;
    color: var(--system-colors-gray-900, #0D1017);
    font-size: 20px;
    font-weight: 700;
}

ul li p {
    color: var(--system-colors-gray-600, #464D59);
    font-size: 14x;
    font-weight: 500;
    line-height: 28px;
    margin-top: 21px;
}
@media screen and (max-width:990px) {
    ul{
        justify-content: space-around;
    }
    ul li{
        max-width: 400px;
    }
}
</style>