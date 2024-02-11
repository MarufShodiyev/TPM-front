<template>
    <h2 class="page_title">{{ title }}</h2>
</template>

<script setup>
import { defineProps } from "vue";

const page_title = defineProps({
    title: {
        type: String,
        defult: ""
    }
})
const { title } = page_title

</script>
   
<style scoped>
.page_title {
    color: #000;
    font-size: 48px;
    font-weight: 700;
    max-width: 812px;
}
</style>
  