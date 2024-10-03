<template>
    <div>
      <h4>Ứng dụng đếm số</h4>
      <h4>Count: {{ count }}</h4>
    </div>
  </template>
  
  <script setup>
  import { onMounted, onUnmounted, ref } from "vue";
  
  const count = ref(0);
  onMounted(() => {
    setInterval(() => {
      count.value++;
    }, 3000);
  });
  </script>
  
  <style></style>
  