<script setup>
import MyCounter from './MyCounter.vue'

// define the increemnt function

const increment = (count) => {
  count++
}
</script>

<template>
  <MyCounter @up="increment" />
</template>

<style scoped></style>
