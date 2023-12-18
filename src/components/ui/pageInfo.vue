<template>
    <p>{{ title }}</p>
</template>

<script setup>
import { defineProps } from 'vue';
const page_info = defineProps({
    title: {
        type: String,
        defult: ""
    }
})
const { title } = page_info
</script>

<style scoped>
p {
    color: var(--system-colors-gray-800, #1C232C);
    font-size: 16px;
    font-weight: 500;
    line-height: 36px;
}
</style>