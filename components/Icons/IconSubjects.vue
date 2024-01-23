<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["nome"]);
const barraAtiva = ref(false);

const toggleAtivo = () => {
  barraAtiva.value = !barraAtiva.value;
};
</script>

<template>
  <div class="icone" >
    <svg
      class="svg-mn"
      width="150"
      height="153"
      viewBox="0 0 160 153"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M52 13H13V140.5H147.5V13H92.5M52 13V78.5L72.25 68.5L92.5 78.5V13M52 13H92.5"
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