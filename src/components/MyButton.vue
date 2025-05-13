<script setup>
import { useAttrs } from 'vue';

const props = defineProps(["contoh"]);
console.info(props);

const attrs = useAttrs();
console.info(attrs);

</script>

<template>
  <button>My Button : {{ attrs.name }}</button>
</template>


<style scoped>

</style>