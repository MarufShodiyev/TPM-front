<template>
    <button>
        <a href="">{{props.label}}</a>
    </button>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps({
    label: {
        type: String,
        default: ""
    }
})

</script>

<style scoped>
button {
    padding: 10px 32px;
   
    border-radius: 15px;
    background: var(--additional-colors-indigo-500, #6265F0);
    border: none;
}
button a{
    color: var(--black-white-white, #FFF);
    font-size: 16px;
    font-weight: 400;
}
</style>