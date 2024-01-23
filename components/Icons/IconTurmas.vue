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
      width="226"
      height="175"
      viewBox="0 0 226 175"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M159.5 162H213.5C213.5 136.508 192.834 115.842 167.342 115.842H164.356C161.327 115.842 158.366 116.134 155.5 116.691C152.557 117.263 149.714 118.114 147 119.216M13 162V162C13 124.016 43.7918 93.2246 81.7754 93.2246H86.2246C124.208 93.2246 155 124.016 155 162V162H13ZM181.621 77.8855C181.621 69.175 174.56 62 165.849 62C157.138 62 150.077 69.175 150.077 77.8855C150.077 86.5961 157.138 93.7711 165.849 93.7711C174.56 93.7711 181.621 86.5961 181.621 77.8855ZM107.5 36.6695V36.6695C107.5 49.6482 96.9787 60.3389 84 60.3389V60.3389C71.0213 60.3389 60.5 49.6482 60.5 36.6695V36.6695C60.5 23.6908 71.0213 13 84 13V13C96.9787 13 107.5 23.6908 107.5 36.6695Z"
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