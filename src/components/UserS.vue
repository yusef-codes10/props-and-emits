<script setup>
// we have to define the props in the child compinent, for it to recieve data
// from the container/parent
import { defineProps, defineEmits } from 'vue'

defineProps({
  firstName: String,
  lastName: String,
  department: String,
  age: Number,
})

const emit = defineEmits(['rm'])
</script>

<template>
  <ul>
    <li>
      firstname: <b>{{ firstName }}</b>
    </li>
    <li>
      lastname <b>{{ lastName }}</b>
    </li>
    <li>
      departement <b>{{ department }}</b>
    </li>
    <li>
      age <b>{{ age }}</b>
    </li>
  </ul>
  <button @click="emit('rm', firstName)">Delete User</button>
</template>

<style scoped></style>
