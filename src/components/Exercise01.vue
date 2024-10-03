<template>
    <h1>Bài tập 01</h1>
</template>

<script setup>
import { onBeforeMount, onMounted } from 'vue';
  onBeforeMount(()=>{
    console.log("onBeforeMount được gọi");
  })
  onMounted(()=>{
    console.log("onMounted được gọi");
  })
</script>

<style>

</style>