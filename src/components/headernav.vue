<template>
    <header>
        <div class="container">
            <div class="header-wrapper">
                <div class="logo">
                    <img src="../assets/images/logo.svg" alt="logo img">
                </div>
                <nav>
                    <ul class="navs">
                        <li v-for="(item, index) in navs" :key="index"><a :href="item.path">{{ item.text }}</a></li>
                    </ul>
                </nav>
                <div class="language_contact">
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
                    <button id="menu" @click="Menu" v-if="open">
                        <i class="fa-solid fa-bars"></i>
                    </button>
                    <button id="menu" @click="Menu" v-if="!open">
                        <i class="fa-solid fa-xmark"></i>
                    </button>

                </div>
            </div>
        </div>
    </header>
    <MenuHeader v-if="!open" :class="{ 'active': !open }" />
</template>



<script setup>
import MenuHeader from './menu.vue'
import { reactive, ref } from 'vue';

let open = ref(true)

const Menu = () => {
    console.log("click me");
    open.value = !open.value;

};

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
]
)

</script>

<style scoped>
header .header-wrapper {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 120px;
}

/* .header-wrapper::before {
    position: absolute;
    content: '';
    width: 800px;
    height: 800px;
    flex-shrink: 0;
    border-radius: 500px;
    background: rgba(226, 41, 0, 0.07);
    filter: blur(100px);
    left: -30%;
    
} */

ul {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

ul li a {
    color: #000;
    font-size: 16px;
    font-weight: 400;
    padding: 10px 32px;
}
ul li a:hover{
    background-color: #6265F0;
    color: white;
    border-radius: 10px;
    transition: background-color 0.5s, color 0.7s;
}

.language_contact {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 45px;
}

.language {
    display: flex;
    align-items: center;
    justify-content: space-between;
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
    justify-content: space-between;
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

/*
#menu{
        display: none;
    width: 35px;
    height: 35px;
    display: flex;
    align-items: center;
    justify-content: center;
} */
button{
    display: none;
    border:none;
    background: none;
    width: 35px;
    height: 35px;
    
}
button i {
    font-size: 30px;
    color: #aeafec;
}

@media screen and (max-width:1242px) {
    ul li a {
        padding: 8px 22px;
    }
}

@media screen and (max-width:1160px) {
    ul li a {
        padding: 5px 15px;
    }

    .language_contact {
        gap: 30px;
    }
}

@media screen and (max-width:1075px) {
    ul li a {
        padding: 5px 10px;
    }

    .language_contact {
        gap: 20px;
    }
}

/* menu qismi responsive */

.active {
    position: absolute;

}

@media screen and (max-width:992px) {
    nav {
        display: none;
    }

    .language_contact {
        gap: 30px;
    }

    .language,
    .contact {
        padding: 8px 16px;
    }



    button{
        display: inline-block;
    }

    
}
</style>
