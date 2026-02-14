<script setup>
// we have to define the props in the child compinent, for it to recieve data
// from the container/parent
import { defineProps } from 'vue'

defineProps({
  firstName: String,
  lastName: String,
  department: String,
  age: Number,
})
</script>

<template>
  <ol>
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
  </ol>
</template>

<style scoped></style>
