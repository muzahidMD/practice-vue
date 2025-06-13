<script setup>
// SAARC country list 

import { ref } from 'vue';
import CountriesComponent from './components/CountriesComponent.vue';

const saarcCountries = ref([
  { name: "Bangladesh", population: 160, capital: "Dhaka" },
  { name: "India", population: 1300, capital: "New Delhi" },
  { name: "Pakistan", population: 160, capital: "Islamabad" },
  { name: "Sri Lanka", population: 160, capital: "Colombo" },
  { name: "Nepal", population: 160, capital: "Kathmandu" },
  { name: "Bhutan", population: 160, capital: "Thimphu" },
  { name: "Maldives", population: 160, capital: "Male" },
  { name: "Afghanistan", population: 160, capital: "Kabul" },
]);

function addCountry() {
  saarcCountries.value.push({ name: 'X', population: '100', capital: 'Y' })
}
</script>

<template>
  <h1>List Of Countries</h1>
  <p>{{ saarcCountries }}</p>
  <countries-component :countries="saarcCountries" />
  <button @click="addCountry()">Add Country</button>
</template>

<style scoped></style>