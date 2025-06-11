<script setup>
// Tow way data binding in input with reactive function
import { reactive, ref } from 'vue';
const person = reactive({
  firstName: "John",
  lastName: "Doe"
})

function changeName() {
  console.log("Changing Name")
  person.firstName = "Rahim";
  person.lastName = "Uddin"
}
</script>

<template>
  <header>
    <p>
      His name is {{ person.firstName }} <br>
      His name is {{ person.lastName }} <br>
    </p>
    <p>
      {{ person }}
    </p>
    <p>
      First name: <input type="text" v-model="person.firstName">
    </p>
    <p>
      Last name: <input type="text" v-model="person.lastName">
    </p>
  </header>

  <main>
    <button @click="changeName()">Change Name</button>
  </main>
</template>

<style scoped></style>
