<script setup>
  import { reactive } from 'vue';
  import Cabecalho from './components/Cabecalho.vue';
  import Formulario from './components/Formulario.vue';
  import Rodape from './components/Rodape.vue';


const estado = reactive({
  numero1: 0,
  numero2: 0,
  resultado: 0,
  operador: 'somar',
})

function getNumber1(evento){
  estado.numero1 = parseFloat(evento.target.value) || 0;
  getOperacao();
}

function getNumber2(evento){
  estado.numero2 = parseFloat(evento.target.value) || 0;
  getOperacao();
}

function getOperador(evento){
  estado.operador = evento.target.value;
  getOperacao();
}

const getOperacao = () => {
  switch (estado.operador){
    case 'subtract':
      estado.resultado = estado.numero1 - estado.numero2;
      break;
    case 'add': estado.resultado = estado.numero1 + estado.numero2;
      break;
    case 'divide':
      estado.resultado = estado.numero2 !== 0 ? estado.numero1 / estado.numero2 : "Digite um divisor diferente de 0"
      break;
    case 'multiply':
      estado.resultado = estado.numero1 * estado.numero2;
      break;
  }
};



</script>

<template>
  <div class="container">
    <Cabecalho />
    <Formulario 
      :get-Number1="getNumber1" 
      :get-Number2="getNumber2"
      :get-Operador="getOperador"     
      :resultado="estado.resultado"
      />
    <Rodape /> 

  </div>
</template>

<style scoped>


</style>
