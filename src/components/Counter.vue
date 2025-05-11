<script setup>
import { ref, nextTick } from 'vue';

const props = defineProps(["name", "initialCount"]);

console.log(`Load Counter component`);
let counter = ref({
    count: 0,
    name: "Syahrul"
});

async function increment(){
  
    console.info(`Incrementing count: ${counter.value.count}`);
    counter.value = {
        name: counter.value.name,
        count: counter.value.count + 1
    };

    await nextTick();
    counter.value.count++;
    await nextTick();
    counter.value.count++;
    await nextTick();

    console.log("Incremented count after nextTick ");
    
  }
</script>

<template>
    <div>
        <h1 id="count"> Counter {{ props.name }} : {{ counter.count }}</h1>
        <button v-on:click="increment">Increment</button>
    </div>
</template>

<style scoped>

</style>