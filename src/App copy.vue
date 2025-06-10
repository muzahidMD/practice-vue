<script setup>
// compute property
import { ref, computed } from 'vue'

const firstName = ref("John");
const lastName = ref("Doe");

const getFullName = () => {
  console.log('Function Called');
  return `${firstName.value} ${lastName.value}`;
}

const computedFullName = computed(() => {
  console.log('Computed Called');
  return `${firstName.value} ${lastName.value}`;
});

function changeName() {
  console.log('Changing Name')
  firstName.value = "Rahim";
  lastName.value = "Uddin";
}

</script>

<template>
  <header>
    <p class="wrapper">
      Your name is <em> {{ firstName }} {{ lastName }}</em><br>
      <button @click="changeName()">Change Name</button>
    </p>
    <p>My name is {{ getFullName() }}</p>
    <p> Your Full name is = {{ getFullName() }} </p></br>
    <p> Your Full name is = {{ getFullName() }} </p></br>
    <p> Your Full name is = {{ getFullName() }} </p></br>
    <p>Your computed Full name is = {{ computedFullName }}</p></br>
    <p>Your computed Full name is = {{ computedFullName }}</p></br>
    <p>Your computed Full name is = {{ computedFullName }}</p></br>
    <p>Your computed Full name is = {{ computedFullName }}</p></br>

  </header>

  <main>
    .
  </main>
</template>

<style scoped></style>
