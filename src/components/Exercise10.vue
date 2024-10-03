<template>
    <h4>Thời gian hiện tại: {{ h }}:{{ m }}:{{ s }} </h4>
  </template>
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  const h = ref(0);
  const m = ref(0);
  const s = ref(0);
  const updateTime = () => {
    const today = new Date();
    h.value = today.getHours();
    m.value = today.getMinutes();
    s.value = today.getSeconds();
  };
  onMounted(() => {
    updateTime();
    setInterval(updateTime, 1000);
  });
  onUnmounted(() => {
    clearInterval();
  });
  </script>
  
  <style>
  </style>
  