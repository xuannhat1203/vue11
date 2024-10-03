<template>
</template>

<script setup>
import {onUpdated } from 'vue';

    const props = defineProps(["sentAge"]);
    onUpdated(()=>{
        alert("Giá trị của biến age đã thay đổi")
    })
</script>

<style>

</style>