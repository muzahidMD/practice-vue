<script setup>
const props = defineProps(['person'])

function changeNames() {
    console.log("changing name")
    props.person.firstName = "Muzahidul";
    props.person.lastName = "Islam";
}
</script>

<template>
    <hr>
    <p>Person Component X</p>
    <p>First Name: {{ person.firstName }}</p>
    <p>Last Name: {{ person.lastName }}</p>
    <input type="text" v-model="person.firstName">
    <input type="text" v-model="person.lastName">
    <button @click="changeNames()">Change name</button>
</template>

<style scoped></style>