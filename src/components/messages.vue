<template>
    <div class="messages">
        <div class="container">
            <div class="messages_wrapper">
                <div class="message_img">
                    <img src="../assets/icons/messages_img.svg" alt="messages img">
                </div>
                <div class="messages_info">
                    <Title title="All messages will be sent to you in 3 different forms!" />
                    <PageInfo id="page_info"
                        title="Elevate your property investment experience as we handle every detail with precision, from tenant relations to maintenance, ensuring your peace of mind. Trust us to navigate the complexities of property management, so you can focus on what matters most. " />
                    <div class="networks">
                        <div class="network">
                            <div class="network_icon">
                                <img src="../assets/icons/sms.svg" alt="sms svg">
                            </div>
                            <h4>SMS</h4>
                        </div>
                        <div class="network">
                            <div class="network_icon">
                                <img src="../assets/icons/tg.svg" alt="tg svg">
                            </div>
                            <h4>Telegram</h4>
                        </div>
                        <div class="network">
                            <div class="network_icon">
                                <img src="../assets/icons/email.svg" alt="email svg">
                            </div>
                            <h4>Email</h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import Title from './ui/title.vue'
import PageInfo from './ui/pageInfo.vue'
</script>

<style>
.messages {
    margin-top: 120px;
}

.messages_wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.message_img img {
    max-width: 750px;
    max-height: 600px;
}

#page_info {
    margin-top: 30px;
    line-height: 28px;
}

.networks {
    display: flex;
    align-items: center;
    gap: 60px;
    padding-top: 54px;
}

.network {
    display: flex;
    align-items: center;
    gap: 22px;
}

.network_icon {
    display: flex;
    width: 52px;
    height: 52px;
    padding: 1px 0px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    background: var(--additional-colors-indigo-50, #EEF2FF);
}
@media screen and (max-width:992px){
    .messages_wrapper{
        flex-direction: column-reverse;
    }
    .messages_info{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        text-align: center;
        margin: 0px auto;
    }
    .networks{
        text-align: center;
        margin: 0px auto;
        justify-content: center;
        padding-bottom: 55px;
    }
    }
</style>
