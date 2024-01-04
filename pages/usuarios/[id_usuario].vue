<script setup>
import IconExit from "~/components/Icons/IconExit.vue";
import IconAdd from "~/components/Icons/IconAdd.vue";
</script>

<template>
  <div>
    <IconExit class="ex" />
    <Menu />
    <section class="">
      <!-- Passar tudo que tem no arquivo Menu.vue para está page, pois irá facilitar a iteração com o button e facilitar
      a minha lógica no código. -->
      <Profile />
      <Information />
    </section>
  </div>
</template>
<style scoped>
.none {
  display: none !important;
}
</style>
 
