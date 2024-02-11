<template>
    <div class="menu-header">
        <ul>
            <li v-for="(value, index) in navs" :key="index"><a :href="value.path">{{ value.text }}</a></li>
        </ul>
        <div class="language">
            <img src="../assets/images/language_img.svg" alt="language_img">
            <select name="language" id="language">
                <option value="Eng">English</option>
                <option value="UZB">Uzbek</option>
                <option value="RUS">Russi</option>
            </select>
        </div>
        <div class="contact">
            <img src="../assets/images/contact.svg" alt="">
            <a href="tel:+998943330799">+998943330799</a>
        </div>
    </div>
</template>
<script setup>
import { reactive } from "vue";
const navs = reactive([
    {
        text: "About Us",
        path: "#about"
    }, {
        text: "Services",
        path: "#services"
    }, {
        text: "Partners",
        path: "#partners"
    }, {
        text: "Contacts",
        path: "#contact"
    }
])
</script>

<style scoped>
@keyframes slideOutList {

    10%,
    90% {}

}

.menu-header {
    position: absolute;
    background-color: #cac5c5;
    top: 0px;
    width: 100%;
    z-index: 2;
    padding: 20px 0px;
    transform: translate(0px, 100px);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 20px;

}

.menu-header ul {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

}

.menu-header ul li {
    padding: 20px 0px;
    cursor: pointer;

}

.menu-header ul li a:hover {
    background: blue;
    padding: 15px 10px;
    border-radius: 10px;
}

.menu-header ul li a {
    color: #000;
    font-size: 20px;
    font-weight: 400;
}
.language {
    display: flex;
    align-items: center;
    /* justify-content: space-between; */
    padding: 10px 24px;
    border-radius: 50px;
    border: 1px solid var(--system-colors-gray-200, #E0E3E6);
    background: var(--black-white-white, #FFF);
    gap: 10px;
}
.language select {
    border: none;
    color: var(--system-colors-gray-500, #636C79);
    font-size: 16px;
    font-weight: 400;
}
.contact {
    display: flex;
    align-items: center;
    /* justify-content: space-between; */
    padding: 10px 24px;
    border-radius: 15px;
    background: var(--additional-colors-indigo-500, #6265F0);
    gap: 10px;
}

.contact a {
    color: var(--black-white-white, #FFF);
    font-size: 16px;
    font-weight: 400;
}
</style>