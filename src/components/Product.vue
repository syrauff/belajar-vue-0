<script setup>
import { ref, watch } from 'vue';

const productId = ref("");
const product = ref(null);

watch(productId, async (newVal, oldVal) => {
    if (newVal) {
        const response = await fetch(`/${newVal}.json`);
        product.value = await response.json();
    } else {
        product.value = null;
    }
});
</script>

<template>
    <label for="productId">
        Product ID:
        <select v-model="productId">
            <option value="">Select a product</option>
            <option value="product1">Product 1</option>
            <option value="product2">Product 2</option>
            <option value="product3">Product 3</option>
        </select>
    </label>

    <div v-if="product">
        <h1>Product</h1>
        <p>Id: {{ product.id }}</p>
        <p>Name: {{ product.name }}</p>
        <p>Price: {{ product.price }}</p>
    </div>
</template>

<style scoped>

</style>