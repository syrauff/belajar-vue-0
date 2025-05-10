<script setup>
console.info('Hello vue3 + Vite + HMR!')

const hello = '<h1>Hello Vue</h1>'
const classHello = 'hello'
const id = "hello"

</script>

<template>
  <h1 :id="id" v-bind:class="classHello">{{ hello }}</h1>
  <div :class="classHello" v-html="hello"></div>

</template>

<style scoped>
.hello {
  color: green;
}
</style>
