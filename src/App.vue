<script setup>
import { ref } from 'vue';

import Numeros from './components/Numeros.vue';
import Operadores from './components/Operadores.vue';
import Resultados from './components/Resultados.vue';

const valor1 = ref('');
const valor2 = ref('');
const operacao = ref('');
</script>

<template>
  <div class="container mt-5">
    <h3>Vue Calc</h3>
    <div class="number-box">
      <p>Primeiro valor:</p>
      <Numeros v-model="valor1" />
    </div>
    <div class="number-box">
      <p>Segundo valor:</p>
      <Numeros v-model="valor2" />
    </div>
    <div class="number-box">
      <p>Escolha a operação:</p>
      <Operadores v-model="operacao" />
    </div>
    <div class="number-box">
      <p>Resultado:</p>
      <Resultados :valor1="valor1" :valor2="valor2" :operacao="operacao" />
    </div>
  </div>
</template>

<style scoped>
.container p {
  color: #2a323d;
}

.container h3 {
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 4px;
  text-align: center;
  color: #2263b9;
}

.number-box {
  width: 100%;
  margin-top: 20px;
  text-align: center;

}
</style>
