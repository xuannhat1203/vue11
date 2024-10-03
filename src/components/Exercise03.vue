<template>
    <div>
        <h3>Current Company: {{ company }}</h3>
        <h3>Age: {{ age }}</h3>
        <button @click="handleRandom">Random</button>
    </div>
</template>

<script setup>
import { onBeforeUpdate, onUpdated, ref } from 'vue';

const company = ref("Rikkei Academy");
const age = ref(1);

const handleRandom = () => {
    const companies = ["Rikkei Academy", "Rikkei Academy2", "Rikkei Academy3"];
    company.value = companies[Math.floor(Math.random() * companies.length)]; 
    age.value = Math.floor(Math.random() * 10) + 1; 
}
onBeforeUpdate(() => {
  console.log("onBeforeUpdate Company:", company.value, "Age:", age.value);
});

onUpdated(() => {
  console.log("onUpdated. Company:", company.value, "Age:", age.value);
});
</script>

<style>

</style>
