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
  <div class="container-sm text-center mt-4">
    <h1 class="mb-4 fw-light text-uppercase">Vue Calc</h1>
    <div class="row">
      <div>
        <p class="fw-bold">Primeiro valor:</p>
        <Numeros v-model="valor1" />
      </div>
      <div>
        <p class="fw-bold">Segundo valor:</p>
        <Numeros v-model="valor2" />
      </div>
      <div>
        <p class="fw-bold">Escolha a operação:</p>
        <Operadores v-model="operacao" />
      </div>
      <div>
        <p class="fw-bold">Resultado:</p>
        <Resultados :valor1="valor1" :valor2="valor2" :operacao="operacao" />
      </div>
    </div>
  </div>
</template>

<style scoped>
  h1 {
    letter-spacing: 8px;
    color:  rgb(37, 85, 174);
  }

  p {
    color: rgb(37, 85, 174);
  }
</style>
