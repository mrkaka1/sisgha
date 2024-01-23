<script setup>
import { ref, defineProps } from 'vue';

const props = defineProps(['nome']);
const barraAtiva = ref(false);

const toggleAtivo = () => {
  barraAtiva.value = !barraAtiva.value;
};
</script>

<template>
  <div class="icone" >
    <svg
      class="svg-mn"
      width="168"
      height="175"
      viewBox="0 0 168 175"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M13 162H155C155 124.016 124.208 93.2246 86.2246 93.2246H81.7754C43.7918 93.2246 13 124.016 13 162Z"
        fill="none"
      />
      <path
        d="M84 13C96.9787 13 107.5 23.6908 107.5 36.6695C107.5 49.6482 96.9787 60.3389 84 60.3389C71.0213 60.3389 60.5 49.6482 60.5 36.6695C60.5 23.6908 71.0213 13 84 13Z"
        fill="none"
      />
      <path
        d="M13 162H155C155 124.016 124.208 93.2246 86.2246 93.2246H81.7754C43.7918 93.2246 13 124.016 13 162Z"
        stroke="white"
        stroke-width="25"
      />
      <path
        d="M84 13C96.9787 13 107.5 23.6908 107.5 36.6695C107.5 49.6482 96.9787 60.3389 84 60.3389C71.0213 60.3389 60.5 49.6482 60.5 36.6695C60.5 23.6908 71.0213 13 84 13Z"
        stroke="white"
        stroke-width="25"
      />
    </svg>
    <span class="nome">{{ nome }}</span>
  </div>
</template>
<style scoped>
.icone {
  display: flex; /* Coloca o SVG e o nome em uma coluna */
  align-items: center;
  cursor: pointer;
  position: relative;
}

.svg-mn {
  width: 25px;
  height: 25px;
  margin-right: 5px;
}

.nome {
  margin-left: 50px;  /* Adicione margem à esquerda para separação do ícone */
  font-size: 16px;
  text-align: center; /* Centraliza o texto */
}

.ativo {
  color: white;
}
</style>