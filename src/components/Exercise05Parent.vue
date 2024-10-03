<template>
    <div>
        <Exercise05Child v-if="isShow"></Exercise05Child>
        <button @click="handleClick">toggleBlockUser</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import Exercise05Child from './Exercise05Child.vue';
    const isShow = ref(true);
    const handleClick = () => {
        isShow.value = false;
    }
</script>

<style>

</style>