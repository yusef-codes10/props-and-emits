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

const upCount = defineEmits(['up'])
</script>

<template>
  <div class="counter">
    <div class="display">
      <p>{{ count }}</p>
    </div>
    <div class="btns">
      <button>Reset</button>
      <button @click="upCount('up', count)">Up</button>
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
