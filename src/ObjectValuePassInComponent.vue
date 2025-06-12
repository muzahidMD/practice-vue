<script setup>
import { reactive, ref } from 'vue';
import PersonComponentX from './components/PersonComponentX.vue';

const person = reactive({
  firstName: "John",
  lastName: "Doe"
})

function changeNames() {
  console.log("Change name ");
  person.firstName = 'Misbahul';
  person.lastName = "Islam";
}
</script>

<template>
  <div>
    <h1>Main App</h1>
    <p>
      {{ person }}
    </p>
    <p>
      Changing Names From Main App <button @click="changeNames">Change Name</button>
    </p>

  </div>
  <person-component-x :person="person" />
</template>

<style scoped></style>
