<script setup>
import { defineProps, ref } from 'vue'

defineProps({
  count: Number,
  maxCount: {
    type: Number,
    default: 10,
  },
  minCount: {
    type: Number,
    default: 0,
  },
  step: {
    type: Number,
    default: 1,
  },
})

const count1 = ref(0)
const upCount = () => {
  count1.value++
}
</script>

<template>
  <div class="counter">
    <div class="display">
      <p>{{ count1 }}</p>
    </div>
    <div class="btns">
      <button>Reset</button>
      <button @click="upCount">Up</button>
      <button>Down</button>
    </div>
  </div>
</template>

<style scoped>
p {
  font-size: 4rem;
  font-weight: 900;
}
</style>
