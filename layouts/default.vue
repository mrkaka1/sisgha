<script setup>
import { ref } from "vue";
import IconKeyDown from "~/components/Icons/IconKeyDown.vue";
import IconLinks from "~/components/Icons/IconLinks.vue";
import IconCalendar from "~/components/Icons/IconCalendar.vue";
import IconProfile from "~/components/Icons/IconProfile.vue";
import IconSubjects from "~/components/Icons/IconSubjects.vue";
import IconTurmas from "~/components/Icons/IconTurmas.vue";
import IconPerson from "~/components/Icons/IconPerson.vue";
import IconHome from "~/components/Icons/IconHome.vue";
import IconOuters from "~/components/Icons/IconOuters.vue";
import IconAdd from "~/components/Icons/IconAdd.vue";

const isBarraAtiva = ref(false);
const isNomesVisiveis = ref(false);

const toggleBarra = () => {
  isBarraAtiva.value = !isBarraAtiva.value;
  isNomesVisiveis.value = isBarraAtiva.value;
};


</script>

<template>
  <div class="layout" >
    <header class="heade">
      <IconPerson class="svgH" />

      <ul class="ulH">
        <li class="Names">Danilo Escudero</li>

        <p class="p">
          DAPE

          <IconKeyDown class="svg" />
        </p>
      </ul>
    </header>

    <div class="barra-menu" @click="toggleBarra" :class="{ barraAtiva: isBarraAtiva }">
      <ul :class="{ barraAtiva: isBarraAtiva }">
        <li>
          <IconHome :nome="isNomesVisiveis ? 'Home' : ''" />
        </li>

        <li>
          <IconTurmas :nome="isNomesVisiveis ? 'Turmas' : ''" />
        </li>

        <li>
          <IconSubjects :nome="isNomesVisiveis ? 'Subjects' : ''" />
        </li>

        <li>
          <IconProfile :nome="isNomesVisiveis ? 'Profile' : ''" />
        </li>
        <li>
          <IconLinks :nome="isNomesVisiveis ? 'Links' : ''" />
        </li>

        <li>
          <IconCalendar :nome="isNomesVisiveis ? 'Calendar' : ''" />
        </li>

        <li>
          <IconOuters :nome="isNomesVisiveis ? 'Outers' : ''" />
        </li>

       <li>
        <IconsIconGear :nome="isNomesVisiveis ? 'Gear' : ''"/>
       </li>
      </ul>
    </div>
    <div class="conteudo">
      <slot></slot>
    </div>
  </div>
</template>

<style>
.layout {
  display: grid;
  grid-template-rows: auto 1fr;
  grid-template-columns: auto 1fr;
  height: 100vh;
}

.heade {
  grid-row: 1/2;
  grid-column: 1/-1;
}



.conteudo {
  grid-row: 2/3;
  grid-column: 2/3;

  padding: 1rem;

  overflow: auto;
}

.heade {
  display: flex;
  height: 70px;
  margin: 0px 0px 1px 0px;
  border-bottom: 0.2px solid #ffffff;
  /* box-shadow: 0px 0.1px 3px #39A048; */
  box-shadow: 0px 0.1px 9px 1px rgba(57, 160, 72, 0.19);
}

.heade .svgH {
  width: auto;
  height: auto;
  margin: 10px 10px 10px 15px;
}

.heade .ulH {
  margin: 0px;
  margin-left: 8px;
  margin-top: 10px;
  padding: 0px;
}

.heade .Names {
  display: block;
  font-weight: bold;
  margin: 0px;
}

.heade .svg {
  width: 10px;
  height: 15px;
  margin-left: 45px;
  margin-top: -21px;
}

.heade .p {
  margin: 0px;
}

.barra-menu {
  align-items: center;
  justify-content: center;
  background-color: #39a048;
}

.barra-menu .svg-mn {
  padding: 0px;
  margin: 15px;
  margin-top: 35px;
  margin-bottom: 25px;
  width: 25px;
  height: 25px;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

</style>
