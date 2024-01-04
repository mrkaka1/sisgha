

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
