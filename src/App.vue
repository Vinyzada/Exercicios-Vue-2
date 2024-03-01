<script setup>
import { ref } from 'vue'

const contador = ref(0)

function Subtrair() {
  contador.value > 0 ? contador.value-- : null
}

const nome = 'Viny'
const idade = 16

function inverter(texto) {
  return texto.split('').reverse().join('').toUpperCase()
}

function saudacao() {
  return `Olá, ${nome}!`
}

function colorAlert() {

}
</script>

<template>
  <div class="info">
    <h1>Informações na tela</h1>
    <p>Nome: {{ nome }} </p>
    <p>Idade: {{ idade }} anos</p>
    <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
    <p>O nome tem {{ nome.length }} caracteres</p>
    <p>O nome invertido é: {{ inverter(nome) }} </p>
    <p> Exemplo de saudação usando função</p>
    <p> {{ saudacao() }} </p>
  </div>
  <br>
  <div class="info">
    <h1>Contador de clicks</h1>
    <button @click="contador++">+</button>
    <button @click="Subtrair()">-</button>
    <button @click="contador = 0">Reset</button>
    <p>Contador: {{ contador }}</p>
    <div v-if="contador < 10" id="alertHigh"></div>
    <div v-else id="alertLow"></div>
  </div>
</template>

<style scoped>
.info {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin: 20px 0px;
}
.info button{
  margin: 0px 10px;
  appearance: none;
  border-radius: 5px;
  font-size: 15px;
  border: 1px solid rgb(183, 210, 219);
  background-color: transparent;
  color: rgb(183, 210, 219);
}
.info button:hover{
  background-color: rgb(81, 80, 80);
  transform: translateY(1px);
  transition: all .55s ease;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}

#alertLow {
  background-color: lightgreen;
  height: 20px;
  width: 100%;
}

#alertHigh {
  background-color: red;
  height: 20px;
  width: 100%;
}
</style>
