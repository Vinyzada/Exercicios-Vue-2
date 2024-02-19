<script setup>

  import { ref } from 'vue'
  const contador = ref(0)
  

</script>

<template>
  <button @click="contador++">+</button>
  <button @click="contador--">-</button>
  <p>Contador: {{ contador }}</p>
</template>

<style scoped>
</style>
