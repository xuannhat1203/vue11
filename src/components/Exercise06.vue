<template>
    <div>
      <button @click="handleClick">Increment</button>
      <p>{{ count }}</p>
    </div>
  </template>

  <script setup>
  import { onBeforeUpdate, onUpdated, ref } from 'vue';
  const count = ref(0);
  const handleClick = () => {
    console.log(8888);
    
    count.value++;
  };
  onUpdated(() => {
    document.title = `Count: ${count.value}`;
  });
  </script>
  <style>
  </style>
  