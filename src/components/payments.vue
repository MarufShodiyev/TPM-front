<template>
    <div class="payments">
        <div class="container">
            <div class="payments_wrapper">
                <div class="payments_info">
                    <Title id="title" title="You can pay online for all services" />
                    <p>Download with</p>
                    <div>
                        <img src="../assets/icons/googlePlay.svg" alt="googlePlay.svg">
                        <img src="../assets/icons/appstore.svg" alt="appstore.svg">
                    </div>
                </div>
                <div class="payments_img">
                    <img src="../assets/images/phone_14_cam_01 2.png" alt="phone_14_cam_01 2.png">
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import Title from './ui/title.vue'
</script>

<style scoped>
.payments {
    background: var(--additional-colors-indigo-500, #6265F0);
    padding-bottom: -3px;
}

.payments_wrapper {
    display: flex;
    align-items: start;
    justify-content: space-between;
    margin-top: 153px;
}

.payments_info {
    padding: 127px 0px;
}

#title {
    color: var(--black-white-white, #FFF);
    
    max-width: 600px;
}

.payments_info p {
    color: var(--black-white-white, #FFF);
    font-size: 20px;
    font-weight: 700;
    margin-top: 30px;
}

.payments_info div {
    padding-top: 17px;
    display: flex;
    gap: 24px;
}

.payments_img {
   margin-top: -100px;
   padding-top: 15px;
   
}

.payments_img img {
    max-width: 500px;
    height: 580px;
}

@media screen and (max-width:992px) {
    .payments_wrapper {
        flex-direction: column;
        justify-content: center;
        text-align: center;
        margin: 0px auto;
       
    }
    .payments_info{
        justify-content: center;
        margin: 0px auto;
        padding: 20px 0px;
    }
    .payments_info div {
        align-items: center;
        justify-content: center;
        text-align: center;
        margin: 0px auto;
    }

    .payments_img{
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0px auto;
        
    }
    .payments_img img{
        max-width: 400px;
        max-height: 370px;
        text-align: center;
    }
}</style>