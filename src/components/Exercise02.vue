<template>
    <div>
        <h2>Count: {{ count }}</h2>
        <button @click="handleChange">Click</button>
    </div>
</template>

<script setup>
import { onBeforeUpdate, onUpdated, ref } from 'vue';
    const count = ref(0);
    onBeforeUpdate(()=>{
        console.log(count,2);
    })
    onUpdated(()=>{
        console.log("Dữ liệu đã được thay đổi");
    })
    const handleChange = () => {
        count.value++;
    }
</script>

<style>

</style>