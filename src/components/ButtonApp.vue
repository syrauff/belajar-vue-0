<script setup>
import MyButton from './MyButton.vue';

function clickHandler() {
  alert('Button clicked!');
}

</script>

<template>
  <MyButton class="button" @click="clickHandler" name="syahrul" contoh="ridho"/>
</template>


<style scoped>
.button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}

</style>'