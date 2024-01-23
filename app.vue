<!-- <script>
if (
  localStorage.getItem("color-theme") === "dark" ||
  (!("color-theme" in localStorage) &&
    window.matchMedia("(prefers-color-scheme: dark)").matches)
) {
  document.documentElement.classList.add("dark");
} else {
  document.documentElement.classList.remove("dark");
}
</script> -->

<template>
  <NuxtLayout>
    <NuxtPage />
    <!-- <div class="flex justify-center items-center min-h-screen">
      <Teleport to="#modal">
        <ModalNewUser v-if="show" @close="closeConfirm"></ModalNewUser>
      </Teleport>
      <button @click="openConfirm">Open Confirm Modal</button>

      
    </div> -->
  </NuxtLayout>
  <div id="modal"></div>
</template>

<style>
@import url("./assets/style/globalstyle.css");
</style>
