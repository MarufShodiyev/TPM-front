<template>
    <div id="about">
        <div class="container">
            <div class="about_wrapper">
                <div class="about_img">
                    <img src="../assets/icons/about_img.svg" alt="about_img.svg">
                </div>
                <div class="about_title">
                    <Title class="title" title="About Us" />
                    <PageInfo class="page_info"
                        title="At Town Property Management, we believe in more than just managing properties; we're dedicated to enhancing the entire property ownership experience. With a passion for real estate and a commitment to excellence, we've become the go-to partner for property owners seeking unparalleled service in TPM." />
                    <h3>Our Mission:</h3>
                    <PageInfo class="page_info"
                        title="Empowering property owners to thrive by providing comprehensive and customized property management solutions. We aim to redefine industry standards through integrity, innovation, and a relentless dedication to client success." />
                    <Button class="btn" label="Fill the form" />
                </div>
            </div>
        </div>
    </div>
</template>


<script setup>
import Title from './ui/title.vue'
import PageInfo from './ui/pageInfo.vue'
import Button from './ui/button.vue'
</script>

<style scoped>
#about {
    position: relative;
}

/* #about::before {
    position: absolute;
    content: "";
    top: -100%;
    right: -10%;
    width: 800px;
    height: 800px;
    flex-shrink: 0;
    border-radius: 500px;

    z-index: 200;
    background: rgba(0, 50, 226, 0.10);
    filter: blur(100px);
    
} */

.about_wrapper {
    margin-top: 113px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 30px;
}

.about_title h3 {
    color: var(--system-colors-gray-800, #1C232C);
    font-size: 20px;
    font-weight: 700;
    margin-top: 32px;
}

.page_info {
    margin-top: 32px;
}

.btn {
    margin-top: 32px;
}

.about_img img {
    max-width: 700px;
    max-height: 500px;
}

@media screen and (max-width:990px) {
    .about_wrapper {
        flex-direction: column-reverse;
        text-align: center;
        margin: 0px auto;
    }

    .about_title {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    .about_img {
        text-align: center;
        margin: 0px auto;
    }
    @media screen and (max-width:768px){
        .about_img img{
            width: 600px;
            height: 500px;
        }
    }
    @media screen and (max-width:520px){
        .about_img img{
            width: 420px;
            height: 300px;
        }
    }
    @media screen and (max-width:420px){
        .title{
            font-size: 35px;
        }
        .page_info{
            font-size: 20px;
        }
        .about_img img{
            width: 341px;
            height: 241px;
        }
    }
}</style>