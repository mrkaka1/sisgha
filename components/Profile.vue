<script setup>

</script>
<template>
  <div>
    <div class="photoBack"></div>
    <div class="cardProfile">
      <div>Teste</div>
    </div>
    <section class="sctContent">
      <Disponibilidade/>
      <Ensino/>
    </section>
  </div>
</template>
<style scoped>
.photoBack {
  display: flex;
  width: 1200px;
  height: 240px;
  margin-left: 11%;
  margin-top: 50px;
  border-radius: 8px;

  background-color: rgb(142, 142, 153) ;
}

.cardProfile {
  width: 400px;
  height: 200px;
  margin-top: -200px;
  margin-left: 205px;
  background-color: blue;
  z-index: 5;
  border-radius: 8px 8px 0px 0px;
}

.sctContent {
  display: flex;
}

@media (max-width: 1366px) {
  .grid-container {
    grid-template-columns: 1fr 1fr; /* Uma coluna com largura total */
  }
}
</style>
