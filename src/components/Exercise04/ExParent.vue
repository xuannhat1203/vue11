<template>
   <div>
        <h4>Age: {{ age }}</h4>
        <button @click="handleRaise">Increase Age</button>
        <ExChid :sentAge="age"></ExChid>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import ExChid from './ExChid.vue';
    const age = ref(1);
    const handleRaise = () => {
        age.value++;
    }
</script>

<style>

</style>