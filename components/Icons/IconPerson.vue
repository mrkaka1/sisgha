<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["nome"]);
const barraAtiva = ref(false);

const toggleAtivo = () => {
  barraAtiva.value = !barraAtiva.value;
};
</script>

<template>
  <div class="icone">
    <svg
      width="40"
      height="41"
      viewBox="0 0 40 41"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <circle cx="20" cy="20.5" r="20" fill="#39A048" />
      <path
        d="M20.0265 13H20.5882C21.7688 13 22.7259 13.9571 22.7259 15.1378C22.7259 16.3184 21.7688 17.2755 20.5882 17.2755H20.0265C18.8458 17.2755 17.8887 16.3184 17.8887 15.1378C17.8887 13.9571 18.8458 13 20.0265 13Z"
        fill="white"
      />
      <path
        d="M13 26.4573H27.6146C27.6146 23.0267 24.8336 20.2457 21.403 20.2457H19.2116C15.781 20.2457 13 23.0267 13 26.4573Z"
        fill="white"
      />
      <path
        d="M20.0265 13H20.5882C21.7688 13 22.7259 13.9571 22.7259 15.1378C22.7259 16.3184 21.7688 17.2755 20.5882 17.2755H20.0265C18.8458 17.2755 17.8887 16.3184 17.8887 15.1378C17.8887 13.9571 18.8458 13 20.0265 13Z"
        stroke="white"
        stroke-width="2.85235"
      />
      <path
        d="M13 26.4573H27.6146C27.6146 23.0267 24.8336 20.2457 21.403 20.2457H19.2116C15.781 20.2457 13 23.0267 13 26.4573Z"
        stroke="white"
        stroke-width="2.85235"
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