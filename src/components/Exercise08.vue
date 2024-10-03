<template>
    <h4>Window Width: {{ width }}px</h4>
  </template>
  
  <script setup>
  import { onMounted, onUnmounted, ref } from 'vue';
  
  const width = ref(window.innerWidth);
  
  const updateWidth = () => {
    width.value = window.innerWidth;
  };
  onMounted(() => {
    window.addEventListener('resize', updateWidth);
  });
  </script>
  
  <style>
  </style>
  