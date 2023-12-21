<template >
    <div id="header_section">
        <div class="container">
            <div class="section__wrapper">
                <div class="header_section-info">
                    <Title class="page_title"
                        title="Unlock Your Town's Potential with Expert Property Management Services" />
                    <p>
                        Elevate your property investment experience as we handle every detail with precision, from tenant
                        relations
                        to maintenance, ensuring your peace of mind. Trust us to navigate the complexities of property
                        management,
                        so you can focus on what matters most.
                    </p>
                    <div id="btn_watch-vidio">
                        <Button label="Fill the form" />
                        <div class="watch-vidio">
                            <a href="https://youtube.com/shorts/a4hMIBKZTJU?si=RWhceWmSjoywrfSu" target="_blank">
                                <img
                                    src="../assets/icons/header_vidio.svg" alt="vatch-vidio.svg"> Watch video</a>
                        </div>
                    </div>
                </div>
                <div class="section_img">
                    <img src="../assets/images/Frame.svg" alt="Frame img">
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import Title from './ui/title.vue';
import Button from './ui/button.vue'
import watchVideo from '../assets/images/video-watch.mp4'
</script>
<style scoped>
#header_section {
    position: relative;

}

.section__wrapper::before {
    position: absolute;
    border-radius: 906px;
    background: rgba(0, 50, 226, 0.10);
    filter: blur(100px);
    top: 50%;
    right: -50px;
    content: '';
    width: 100%;
    height: 100%;
    width: 600px;
    height: 600px;
    flex-shrink: 0;
    z-index: -1;
   
}

.section__wrapper {
    position: relative;
    display: flex;
    align-items: start;
    justify-content: space-between;
    padding-top: 42px;
    gap: 30px;
    background-position: right;
}

div .page_title {
    padding-top: 80px;

}

div p {
    padding: 32px 0px;
    color: var(--system-colors-gray-700, #2F3641);
    font-size: 20px;
    font-weight: 500;
    line-height: 36px;
    max-width: 812px;
}

#btn_watch-vidio {
    display: flex;
    align-items: center;
    gap: 50px;

}


.watch-vidio{
    display: inline-block;
}
.watch-vidio a {
    display: flex;
    align-items: center;
    gap: 32px;
}

.watch-vidio a {
    color: var(--system-colors-gray-700, #2F3641);
    font-size: 16px;
    font-weight: 500;
}


.section_img img {
    padding-bottom: 25px;
    max-width: 750px;
    max-height: 650px;

}

@media screen and (max-width:990px) {
    .section__wrapper {
        flex-direction: column;
       
    }
    .header_section-info,.section_img{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        text-align: center;
        margin: 0px auto;
    }
    #btn_watch-vidio{
        /* display: inline-block; */
        text-align: center;
        margin: 0px auto;
    }
    .section__wrapper{
        top: 35%;
        right: 0px;
    }
    .section__wrapper::before{
        top: 30%;
        right: 23px;
    }
    
}

@media screen and (max-width:768px){
    div .page_title{
        padding-top: 20px;
        font-size: 40px;
    }
    .section_img img{
        max-width: 600px;
        max-height: 500px;
    }
}
</style>
