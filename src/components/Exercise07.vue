<template>
  <input v-model="inputValue" type="text">
</template>

<script setup>
import { onUpdated, ref } from 'vue';
    const inputValue = ref("");
    onUpdated(()=>{
        document.title = inputValue.value
    })
    
</script>

<style>

</style>