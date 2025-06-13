<script setup>
defineProps(['country']);
</script>

<template>
    <li>
        <input type="text" v-model="country.name">
        -<input type="text" v-model="country.population">
        -<input type="text" v-model="country.capital">
    </li>
</template>

<style scoped></style>