<script setup>
import IconExit from "~/components/Icons/IconExit.vue";
</script>
<template>
  <div>
    <IconExit class="ex" />
    <Menu />
    <section class="none">
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

