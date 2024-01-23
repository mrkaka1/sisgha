<script setup>
import { ref } from "vue";

const props = defineProps(["nome"]);
const barraAtiva = ref(false);

const toggleAtivo = () => {
  barraAtiva.value = !barraAtiva.value;
};
</script>
<template>
  <div class="icone" >
    <svg
      class="home"
      width="26"
      height="60"
      viewBox="0 0 168 174"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M13 70.9183V157C13 159.209 14.7909 161 17 161H56.5C58.7091 161 60.5 159.209 60.5 157V116.5C60.5 114.291 62.2909 112.5 64.5 112.5H103.5C105.709 112.5 107.5 114.291 107.5 116.5V157C107.5 159.209 109.291 161 111.5 161H151C153.209 161 155 159.209 155 157V70.9183C155 69.7055 154.45 68.5583 153.504 67.7991L86.5041 14.0104C85.0413 12.8359 82.9587 12.8359 81.4959 14.0104L14.4959 67.7991C13.5502 68.5583 13 69.7056 13 70.9183Z"
        stroke="white"
        stroke-width="25"
      />
    </svg>

    <span  class="nome">{{ nome }}</span>
  </div>
</template>

<style scoped>
.home {
  margin-left: 13px;
  cursor: pointer;
}

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
