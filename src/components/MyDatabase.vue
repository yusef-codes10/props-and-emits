<script setup>
// this is the parent/container component that handles the children.

import { ref } from 'vue'
import UserS from './UserS.vue'
const database = ref([
  { firstName: 'Peter', lastName: 'Parker', department: 'Marketing', age: 23 },
  { firstName: 'Mary Jane', lastName: 'watson', department: 'Marketing', age: 22 },
  { firstName: 'Harry', lastName: 'Osborn', department: 'Scince', age: 23 },
  { firstName: 'Gwen', lastName: 'Stacy', department: 'Science', age: 23 },
  { firstName: 'Eddie', lastName: 'Brock', department: 'Science', age: 25 },
  { firstName: 'Liz', lastName: 'Alan', department: 'Bilology', age: 23 },
  { firstName: 'Flash', lastName: 'Tompson', department: 'biology', age: 24 },
])

console.log(database)
</script>

<template>
  <UserS
    v-for="(user, index) in database"
    :key="index"
    :firstName="user.firstName"
    :lastName="user.lastName"
    :department="user.department"
    :age="user.age"
  />
</template>

<style scoped></style>
