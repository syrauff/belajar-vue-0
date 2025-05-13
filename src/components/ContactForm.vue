<script setup>
const model = defineModel( {
  type: Object,
  required: true,
  get: (value) => {
    value.email = value.email.toUpperCase();
    return value;
  }
})

</script>

<template>
  <h1>Contact Us</h1>
  <form action="">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="model.name" />
    </div>
    <div>
      <label for="email">Email</label>
      <input type="email" id="email" v-model="model.email" />
    </div>
    <div>
      <label for="age">age</label>
      <input type="number" id="age" v-model="model.age" />
    </div>
    <div>
      <label for="type">Type</label>
      <select id="type" v-model="model.type">
        <option value="feedback">Feedback</option>
        <option value="bug">Bug</option>
        <option value="other">Other</option>
      </select>  
    </div>
    <div>
      <label for="complain">complain</label>
      <input type="checkbox" id="complain" v-model="model.complain">
    </div>
    <div>
      <label for="message">Message</label>
      <textarea id="message" v-model="model.message"></textarea>
    </div>
    <button type="submit">Submit</button>
  </form>
</template>


<style>

</style>