<script setup>
import { ref } from 'vue';

console.info(`Load Counter component`);
let count = ref(0);

function increment(){
  
    console.info(`Incrementing count: ${count.value}`);
    count.value++;

    document.getElementById('count').innerText = `Counter : ${count.value}`;
  }
</script>

<template>
    <div>
        <h1 id="count"> Counter : {{ count }}</h1>
        <button v-on:click="increment">Increment</button>
    </div>
</template>

<style scoped>

</style>