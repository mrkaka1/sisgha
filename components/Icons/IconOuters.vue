<script setup>
import { ref } from "vue";

const props = defineProps(["nome"]);
const barraAtiva = ref(false);

const toggleAtivo = () => {
  barraAtiva.value = !barraAtiva.value;
};
</script>
<template>
  <div class="icone">
    <svg
      class="svg-mn"
      width="168"
      height="175"
      viewBox="0 0 168 175"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M13 17V54.5C13 56.7091 14.7909 58.5 17 58.5H54.5C56.7091 58.5 58.5 56.7091 58.5 54.5V17C58.5 14.7909 56.7091 13 54.5 13H17C14.7909 13 13 14.7909 13 17Z"
        stroke="white"
        stroke-width="25"
      />
      <path
        d="M151 13H113.5C111.291 13 109.5 14.7909 109.5 17V54.5C109.5 56.7091 111.291 58.5 113.5 58.5H151C153.209 58.5 155 56.7091 155 54.5V17C155 14.7909 153.209 13 151 13Z"
        stroke="white"
        stroke-width="25"
      />
      <path
        d="M155 158V120C155 117.791 153.209 116 151 116H113.5C111.291 116 109.5 117.791 109.5 120V158C109.5 160.209 111.291 162 113.5 162H151C153.209 162 155 160.209 155 158Z"
        stroke="white"
        stroke-width="25"
      />
      <path
        d="M17 162H54.5C56.7091 162 58.5 160.209 58.5 158V120C58.5 117.791 56.7091 116 54.5 116H17C14.7909 116 13 117.791 13 120V158C13 160.209 14.7909 162 17 162Z"
        stroke="white"
        stroke-width="25"
      />
    </svg>
    <span  class="nome">{{ nome }}</span>
  </div>
</template>

<style scoped>
.icone {
  display: flex; /* Coloca o SVG e o nome em uma coluna */
  align-items: center;
  cursor: pointer;
  position: relative;
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