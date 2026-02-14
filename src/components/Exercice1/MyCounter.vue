<script setup>
import { defineProps, defineEmits } from 'vue'

defineProps({
  count: {
    type: Number,
    default: 0,
  },
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
// !
const emit = defineEmits(['up', 'down', 'reset'])
</script>

<template>
  <div class="counter">
    <div class="display">
      <p>{{ count }}</p>
    </div>
    <div class="btns">
      <button @click="emit('reset')">Reset</button>
      <button @click="emit('up')">Up</button>
      <button @click="emit('down')">Down</button>
    </div>
  </div>
</template>

<style scoped>
p {
  font-size: 4rem;
  font-weight: 900;
}
</style>
