<script setup>
import {inject} from 'vue'

const profile = inject('profile');

</script>

<template>
  <h1>Profile</h1>
    <p>Name: {{ profile.name }}</p>
    <p>email: {{ profile.email }}</p>
</template>

<style scoped>

</style>