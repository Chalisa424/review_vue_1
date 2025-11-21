<script setup>
import { ref, computed } from 'vue';

const priceUSD = ref(1)
const exChangeRate = ref(35)

const priceTHB = computed(() =>{
  return priceUSD.value * exChangeRate.value
})
</script>
<template>
  <div>USD{{ priceUSD }} THB{{ priceTHB }}</div>
  <div>THB<input type="text" v-model="priceTHB "></div>
  <div>USD<input type="text"  v-model="priceUSD"></div>
 
</template>