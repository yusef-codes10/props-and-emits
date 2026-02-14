<script setup>
// this is the parent/container component that handles the children.

import { ref } from 'vue'
const database = ref([])

console.log(database)
</script>

<template>
  <h1>You did it!</h1>
</template>

<style scoped></style>
