<script setup>
// computed property
import { ref, computed } from 'vue'

const number = ref(4);
const doubleNumber = computed(() => {
  return number.value * 2;
})

const squareNumber = computed(() => {
  return number.value * number.value;
})
const cubeNumber = computed(() => {
  return number.value * number.value * number.value;
})
const quadNumber = computed(() => {
  return number.value * number.value * number.value * number.value;
})

function changeNumber() {
  console.log("Changing number")
  number.value = 5;
}
</script>

<template>
  <header>
    <button @click="changeNumber()">Change Number</button>
    <p>This is a number {{ number }}</p>
    <p>This is double Double number = {{ doubleNumber }}</p>
    <p>This is double Square number = {{ squareNumber }}</p>
    <p>This is double Cube number = {{ cubeNumber }}</p>
    <p>This is double Quad number = {{ quadNumber }}</p>
  </header>

  <main>
    .
  </main>
</template>

<style scoped></style>
