<script setup>
import Counter from './Counter.vue';
import CounterStateless from './CounterStateless.vue';
import { ref } from 'vue';

const counter = ref(0);
</script>

<template>
    <Counter name="syahrul" />
    <Counter name="ridho" />

    
    <CounterStateless name="Joko" :counter="counter"/>
    <CounterStateless name="Prabo" :counter="counter"/>
    <button @click="counter++">Increment Counter</button>
</template>


<style>

</style>