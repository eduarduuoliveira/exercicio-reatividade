<script setup>
import { ref, computed } from 'vue'
const contador = ref (10)

const soma = computed(() =>{
  return contador.value + contador2.value
})
const par = computed (()=>{
  return (contador.value + contador2.value) %2 === 0
})

function incrementar (){
  contador.value++
}
function decrementar(){
  if (contador.value > 0)
  contador.value--
}
function reset(){
  contador.value = 0
}

const contador2 = ref (10)

function incrementar2 (){
  contador2.value++
}
function decrementar2(){
  if (contador2.value > 0)
  contador2.value--
}
function reset2(){
  contador2.value = 0
}

</script>

<template>
  <button @click="incrementar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reset">c</button>
  <p>Valor do contador: {{  contador }}</p>
  <div></div>

  <button @click="incrementar2">+</button>
  <button @click="decrementar2">-</button>
  <button @click="reset2">c</button>
  <p>Valor do contador: {{  contador2 }}</p>

</template>

<style scoped>
button {
  margin-left: 10px;
  background-color: brown;
  color: black;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;  
}
</style>