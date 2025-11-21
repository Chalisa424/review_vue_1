<script setup>
import { ref, computed } from 'vue';

const firstname = ref('')
const lastname = ref('')

const fullname = computed(() =>{
  return `${firstname.value} ${lastname.value}`
})
</script>
<template>
  <div>{{ fullname }}</div>
  First Name<input type="text" name="firstname" v-model="firstname">
  Last Name<input type="text" name="lastname" v-model="lastname">
 
</template>