<template>
    <div class="menu-header">
        <ul>
            <li v-for="(value, index) in navs" :key="index"><a :href="value.path">{{ value.text }}</a></li>
        </ul>
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
@keyframes slideOutList{
   10%,
   90%{
    
   }
    
}

.menu-header {
    position: absolute;
    background-color: #cac5c5;
    top: 0px;
    width: 100%;
    z-index: 2;
    padding: 20px 0px;
    transform: translate(0px,100px);
    
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
.menu-header ul li a:hover{
    background: blue;
    padding: 15px 10px;
    border-radius: 10px;
}
.menu-header ul li a{
    color: #000;
    font-size: 20px;
    font-weight: 400;
}
</style>