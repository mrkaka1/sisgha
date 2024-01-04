<template>
  <div class="absolute inset-0 overflow-y-auto bg-black bg-opacity-50 ">
    <div class="flex items-start justify-center min-h-screen mt-24 text-center gap-10">
      <div
        class="modal bg-white text-black rounded-lg text-center shadow-xl p-6 w-64"
        role="dialog"
        aria-modal="true"
      >
        <h1>Cadastrar Usuário</h1>
        <div>
          <ContentModal />
        </div>

        <div class="flex justify-center py-4 text-white">
          <button
            @click="($event) => $emit('close')"
            class="border border-black bg-white text-black mr-4"
          >
            Cancelar
          </button>

          <button @click="($event) => $emit('close')" class="text-black">
            Cadastrar
          </button>
        </div>
      </div>

      <div
        class="modal2 bg-white text-black rounded-lg text-center shadow-xl p-6"
        role="dialog"
        aria-modal="true"
      >
        <h1>Cadastrar Usuário</h1>
        <div>
          <ContentModal2/>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.modal {
  width: 28%;
  height: max-content;
}

h1 {
  font-weight: bold;
}

.modal2 {
  width: 22%;
  height: 529px;
}
</style>
