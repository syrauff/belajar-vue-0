<script setup>
import { provide, reactive } from 'vue';
import Profile from './Profile.vue';
import ProfileAddress from './ProfileAddress.vue';

const profile = reactive({
  name: 'John Doe',
  email: 'john@test.com'
});
provide('profile', profile);

</script>

<template>
  <input type="text" v-model="profile.name" placeholder="Name" />
  <Profile />
  <ProfileAddress />
</template>

<style scoped>

</style>