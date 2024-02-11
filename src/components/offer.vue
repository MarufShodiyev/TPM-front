<template>
    <div id="contact">
        <div class="container">
            <div class="offer_wrapper">
                <Title class="center" title="Get an offer" />
                <PageInfo class="center page_info" title="Lorem ipsum dolor sit amet consectetur. Metus eget risus viverra malesuada faucibus nulla at viverra. Eget ac elementum vel nunc non tempor. 
Nec dignissim massa elementum eu venenatis lorem. Viverra integer nibh tellus morbi sed." />
                <form>
                    <input type="text" placeholder="name" id="name">
                    <input type="text" placeholder="Last name" id="last_name">
                    <input type="tel"   @input="enforcePhoneFormat()" placeholder="Phone number" id="tel_number">
                    <input type="email" placeholder="Email" id="email">
                    <textarea name="messege" id="message" cols="30" rows="7" placeholder="Message"></textarea>
                </form>
                <Button class="offer_btn" label="Send message" />
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
#contact {
    /* background-image: url(../assets/images/offerback.png); */
    background-repeat: no-repeat;
    /* background-position: top; */
    background-position: center;
    margin-top: 30px;
    /* padding: 150px 0px; */
}

.offer_wrapper {
    padding: 100px 0px;
    /* margin-top: 30px; */
}

.center {
    text-align: center;
    margin: 0px auto;
}

.page_info {
    margin-top: 20px;
}

form {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 32px;
    flex-wrap: wrap;
    padding: 60px 0px 30px 0px;

}

form input {
    padding: 18px 20px;
    max-width: 450px;
    border: none;
    border-radius: 10px;
    border: 1px solid var(--system-colors-gray-100, #F1F2F4);
    background: #FFF;
    outline: none;
    width: 100%;
}

form input:focus-visible {
    outline: 1px solid var(--system-colors-gray-100, #5de85d);
}

#message {
    display: flex;
    max-width: 932px;
    padding: 20px;
    align-items: flex-start;
    width: 100%;
    flex-shrink: 0;
    border: none;
    border-radius: 10px;
    border: 1px solid var(--system-colors-gray-100, #F1F2F4);
    background: #FFF;
    outline: none;
}

#message:focus-visible {
    outline: 1px solid var(--system-colors-gray-100, #5de85d);
}

.offer_btn {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 32px auto 0px;
}
@media screen and (max-width:910px){
    form input{
        max-width: 500px;
        width: 100%;
    }
    #message {
        max-width: 500px;
        width: 100%;
    }
}

</style>