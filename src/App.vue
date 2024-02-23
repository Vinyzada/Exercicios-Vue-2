<script setup>

  import { ref } from 'vue'
  const contador = ref(0)
 function Subtrair(){
  contador.value>0 ? contador.value-- : null
 }


</script>

<template>
  <button @click="contador++">+</button>
  <button @click="Subtrair()">-</button>
  <button @click="contador=0">Reset</button>

  <p>Contador: {{ contador }}</p>
</template>

<style scoped>

</style>
