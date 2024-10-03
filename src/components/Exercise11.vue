<template>
    <div>
      <ul>
        <li>Đỏ: {{ red }} giây</li>
        <li>Vàng: {{ yellow }} giây</li>
        <li>Xanh: {{ green }} giây</li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from "vue";
  const red = ref(40);
  const yellow = ref(3);
  const green = ref(60);
  const redCountDown = () => {
    intervalId = setInterval(() => {
      if (red.value > 0) {
        red.value--;
      } else {
       clearInterval();
        greenCountdown(); 
      }
    }, 1000);
  };
  
  const greenCountdown = () => {
    intervalId = setInterval(() => {
      if (green.value > 0) {
        green.value--;
      } else {
       clearInterval();
        yellowCountdown(); 
      }
    }, 1000);
  };
  
  const yellowCountdown = () => {
    intervalId = setInterval(() => {
      if (yellow.value > 0) {
        yellow.value--;
      } else {
       clearInterval()
       redCountDown(); 
      }
    }, 1000);
  };
  onMounted(() => {
    redCountDown(); 
  });
  onUnmounted(() => {
   clearInterval() 
  });
  </script>
  
  <style></style>
  