<script setup>
import { inject } from 'vue';

const profile = inject('profile');
</script>

<template>
  <h1>Profile address : {{ profile.name }}</h1>
  <p>Address ...</p>
</template>

<style scoped>

</style>