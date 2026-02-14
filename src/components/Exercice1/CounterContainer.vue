<script setup>
import MyCounter from './MyCounter.vue'
import { ref } from 'vue'

// define the increemnt function

const count = ref(0)
const increment = () => {
  count.value++
}

const descrement = () => {
  count.value--
}
</script>

<template>
  <MyCounter :count="count" @up="increment" @down="descrement" />
</template>

<style scoped></style>
