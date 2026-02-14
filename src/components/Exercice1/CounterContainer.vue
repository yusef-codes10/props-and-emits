<script setup>
import MyCounter from './MyCounter.vue'
import { ref } from 'vue'

// define the increemnt function

const count = ref(0)
const max = ref(10)
const min = ref(0)
const increment = () => {
  // handle the max here
  if (count.value >= max.value) {
    console.log('you are out of bounds!')
    return
  }
  count.value++
}

const descrement = () => {
  // handel the min here
  if (count.value <= min.value) {
    console.log('too small dude')
    return
  }
  count.value--
}

const reset = () => {
  count.value = 0
}

// handle the max count
// const handleMax = (limit) => {
//   if (limit < 0) {
//     console.log('cannot go beyond 0')
//   }
//   if (limit > count.value) {
//     console.log('you have surpassed the limit')
//   }
// }
</script>

<template>
  <MyCounter :count="count" @up="increment" @down="descrement" @reset="reset" />
</template>

<style scoped></style>
