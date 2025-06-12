<script setup>
// const props = defineProps([
//     'fn',
//     'ln'
// ]);
const fn = defineModel('fn');
const ln = defineModel('ln');

function changingName() {
    console.log("Change Name");
    fn.value = "Rahim";
    ln.value = "Uddin";
}
</script>

<template>
    <hr>
    <p>Person Component</p>
    <p>First Name: {{ fn }}</p>
    <p>Last Name: {{ ln }}</p>
    <button @click="changingName()">Change Name</button><br>
    <p>First Name: <input type="text" v-model="fn"><br></p>
    <p>Last Name:<input type="text" v-model="ln"><br></p>
</template>

<style scoped></style>