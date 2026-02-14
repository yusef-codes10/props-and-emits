<script setup>
import { defineProps } from 'vue'

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
</script>

<template>
  <div class="counter">
    <div class="display">
      <p>0</p>
    </div>
    <div class="btns">
      <button>Reset</button>
      <button>Up</button>
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
