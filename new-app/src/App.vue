<script setup>
import { ref } from 'vue';

const firstname = ref('')
const lastname = ref('')
</script>
<template>
  <div>{{ firstname }} {{ lastname }}</div>
  First Name<input type="text" name="firstname" v-model="firstname">
  Last Name<input type="text" name="lastname" v-model="lastname">
 
</template>