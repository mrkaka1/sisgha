<script setup>
import IconAdd from "~/components/Icons/IconAdd.vue";
</script>
<template>
  <div>
    <SeachBar />
  </div>
  <div>
    <IconAdd/>
  </div>
  <div>
    <section class="content-usuario">
      <div class="ctusu">
        <NuxtLink
          v-for="i in 5"
          :key="i"
          :to="`/usuarios/${i}`"
          class="usuario"
        >
          <div class="circle">
            <img src="../imgs/Photo.png" alt="" />
          </div>
          <h4 class="nomes">Danilo Escudero</h4>
          <h6 class="cargo">Professor</h6>
        </NuxtLink>
      </div>
    </section>
  </div>
</template>

<script setup></script>

<style>
.content-usuario {
  margin-top: 60px;
  margin-left: 150px;
}
.ctusu {
  grid-column: 1/3;
  grid-row: 1;
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
  grid-row: 1;
  margin-top: 50px;
  width: 140px;
  height: 190px;
  border: 2px solid #c8dccb;
  border-radius: 8px;
  align-items: center;
  justify-content: center;
}

.circle {
  margin: 17px;
}

.ctusu {
  display: flex;
  gap: 70px;
}

.nomes {
  color: #000;
  font-size: 0.85rem;
  margin-left: 15px;
  font-weight: 700;
}

.cargo {
  margin-left: 30px;
  font-weight: 450;
  color: #c8dccb;
}

.svgvt {
  width: 12px;
  height: 12px;
  position: relative;
}
</style>
