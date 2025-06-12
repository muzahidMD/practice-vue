<script setup>
import { ref } from 'vue';
import PersonComponent from './components/PersonComponent.vue';
import Counter from './components/Counter.vue';

const firstName = ref("john");
const lastName = ref("Doe");

const changeName = () => {
  console.log("Changing Name");
  firstName.value = "Rashedul";
  lastName.value = "Islam"
}
const count = ref(16); 
</script>

<template>
  <div>
    <h1>Main App</h1>
    <p>
      {{ firstName }} {{ lastName }}
    </p>
    <p>
      Changing Names From Main App <button @click="changeName">Change Name</button>
    </p>
    <P>Count = {{ count }}</P>
    <p>
      <Counter v-model="count" />
    </p>
  </div>
  <person-component v-model:fn="firstName" v-model:ln="lastName" />
</template>

<style scoped></style>
