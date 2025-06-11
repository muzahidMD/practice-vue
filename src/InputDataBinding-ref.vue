<script setup>
// Tow way data binding in input with ref function
import { ref } from 'vue';
const firstName = ref("John");
const lastName = ref("Doe");

function changeName() {
  console.log("Changing Name")
  firstName.value = "Rahim";
  lastName.value = "Uddin"
}
</script>

<template>
  <header>
    <p>
      His name is {{ firstName }} <br>
      His name is {{ lastName }} <br>
    </p>
    <p>
      First name: <input type="text" v-model="firstName">
      <!-- First name: <input type="text" :value="firstName">  -->
    </p>
    <p>
      Last name: <input type="text" v-model="lastName">
      <!-- Last name: <input type="text" :value="lastName"> -->
    </p>
  </header>

  <main>
    <button @click="changeName()">Change Name</button>
  </main>
</template>

<style scoped></style>
