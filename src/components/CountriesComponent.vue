<script setup>
import Country from './Country.vue';
const props = defineProps(['countries'])

</script>

<template>
    <hr>
    <h3>Countries Component</h3>
    <ul>
        <country v-for="country in countries" :key="country.name" :country="country" />
    </ul>
</template>

<style scoped></style>