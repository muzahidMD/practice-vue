<script setup>
const model = defineModel(); 
</script>

<template>
    <hr>
    <p>Counter Component</p>
    <p>Count : {{ model }}</p>
    <button @click="model++">Increment</button>
    <button @click="model--">Decrement</button>
    <button @click="model = 0">Reset</button>
    <input type="number" v-model="model">
</template>

<style scoped></style>