<script setup>
import { useSlots, ref } from 'vue';
// const {title} = defineProps({
//   title: {
//     type: String,
//     default: 'Default Title'
//   }
// })

const slots = useSlots();
const counter = ref(0);
</script>

<template>
  <!-- <h1>{{ title }}</h1> -->
  <div>
    <div v-if="slots.header">
      <slot :counter="counter" name="header">
        <h1>header content</h1>
      </slot>
    </div>
    <div v-if="slots.default">
      <slot :counter="counter" name="default">
        <h1>content default</h1>
      </slot>
    </div>
    <div v-if="slots.footer">
      <slot :counter="counter" name="footer">
        <h1>footer content</h1>
      </slot>
    </div>
    <div>
      <button @click="counter++">Increment</button>
    </div>
  </div>
</template>

<style scoped>

</style>