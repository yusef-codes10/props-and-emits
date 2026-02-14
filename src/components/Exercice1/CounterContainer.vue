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

const reset = () => {
  count.value = 0
}
</script>

<template>
  <MyCounter :count="count" @up="increment" @down="descrement" @reset="reset" />
</template>

<style scoped></style>
