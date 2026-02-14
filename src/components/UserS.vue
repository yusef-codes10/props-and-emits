<script setup>
// we have to define the props in the child compinent, for it to recieve data
// from the container/parent
import { defineProps } from 'vue'

defineProps({
  firstName: String,
  lastName: String,
  department: String,
  age: Number,
})
</script>

<template>
  <ol>
    <li>firstname</li>
    <li>lastname</li>
    <li>departement</li>
    <li>age</li>
  </ol>
</template>

<style scoped></style>
