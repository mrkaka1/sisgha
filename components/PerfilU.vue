<script setup lang="ts">

import IconAdd from "~/components/Icons/IconAdd.vue";
import { ref } from 'vue';
import ModalNewUser from "./ModalNewUser.vue";


const show = ref(false);

const openConfirm = () => show.value = true;


const closeConfirm = () => show.value = false;

</script>


<template>
  <div>
    <SeachBar />
  </div>
  <div>
    <IconAdd class="iconadd" @click="openConfirm"/>
    <Teleport to="#modal">
        <ModalNewUser class="transition" v-if="show" @close="closeConfirm" ></ModalNewUser>
      </Teleport>
  </div>
  
  <div class="contentUsu">
    <section class="content-usuario">
      <div class="ctusu">
        <NuxtLink
          v-for="i in 5"
          :key="i"
          :to="`/usuarios/${i}`"
          class="usuario"
        >
          <div class="photoProfile">
            <IconsIconPersonProfile />
          </div>
          <h4 class="nomesP" >Danilo Escudero</h4>
          <h6 class="cargo">Professor</h6>
        </NuxtLink>
      </div>
    </section>
  </div>
</template>


<style>

.content-usuario {
  margin-left: 150px;
}
.ctusu {
  grid-column: 1/3;
  grid-row: 1;
  margin-top: 50px;
}

.label {
  display: block;
  width: 50px;
  font-size: 10px;
  font-weight: 600;
  background-color: white;
  margin-top: 60px;
  margin-left: 20px;
}

.usuario {
  display: flex;
  flex-direction: column; /* Alinha os itens em coluna (um abaixo do outro) */
  justify-content: center; /* Centraliza verticalmente */
  align-items: center; /* Centraliza horizontalmente */
  margin-top: 50px;
  width: 140px;
  height: 190px;
  border: 2px solid #c8dccb;
  border-radius: 8px;
  align-items: center;
  justify-content: center;
}

.photoProfile {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 100px;
  border: 1px solid #c8dccb;
  border-radius: 8px;
  background-color: #F0F0F0;
  justify-content: center;
  align-content: center;
}

.ctusu {
  display: flex;
  gap: 70px;
}

.nomesP {
  margin-top: 10px;
  color: #000;
  font-size: 0.85rem;
  font-weight: 700;
}

.cargo {
  font-weight: 350;
  color: #c8dccb;
  font-size: 14px;
}

.svgvt {
  width: 12px;
  height: 12px;
  position: relative;
}

.iconadd {
  position: relative;
}



</style>
