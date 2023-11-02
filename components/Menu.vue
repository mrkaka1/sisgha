<template>
  <div>
    <section class="barraperfil">
      <div class="barra">
        <p class="ifor">Informações</p>
        <p class="disp">Disponibilidade</p>
        <!--class="info" class="disp" -->
        <p class="btensi">Ensino</p>
      </div>
    </section>
  </div>
</template>
<style scoped>
.barraperfil {
  margin-top: 45px;
  margin-left: 28%;
}
.barra {
  display: flex;
  gap: 40px;
  margin: 0px;
  width: 600px;
  height: 32px;
  border: 3px solid #c8dccb;
  border-radius: 6px 6px 6px 6px;
  place-content: center;
  align-self: center;
  place-self: center;
  place-items: center;
  font-weight: 600;
  cursor: pointer;
  background-color: #ebf8ef;
}

.ifor,
.btensi {
  padding-top: 2px;
}
</style>
