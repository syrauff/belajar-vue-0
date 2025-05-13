<script setup>
import MyButton from './MyButton.vue';
import Container from './Container.vue';

function clickHandler() {
  alert('Button clicked!');
}

</script>

<template>
  <Container title="My Button wooe">
    <template #header="attributes">
      <h1>Header Content {{ attributes.counter }}</h1>
    </template>
    <template v-slot:default >
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quas, placeat. Et, est optio? Debitis iure quae nobis maxime, assumenda vel!<br>
      <MyButton class="button" @click="clickHandler" name="syahrul" contoh="ridho"/>
    </template>
    <template #footer>
      <h1>copyright</h1>
    </template>
  </Container>
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