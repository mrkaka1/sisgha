<template>
  <div>
    <section class="infor none">
      <h1 class="if">
        Informações
        <div class="elemento"></div>
      </h1>
      <div class="email">
        <span>Email:</span>
        <p>exemplo.institucional@gmail.com</p>
      </div>
      <div class="func">
        <span>Função: </span>
        <p>Professor</p>
      </div>
      <div class="stt">
        <span>Status da Conta: </span>
        <p>Ativo</p>
      </div>
    </section>
  </div>
</template>
<style>
.infor {
   margin-top: 5%;
   margin-left: 28%;
}

.if {
   display: flex;
}
.elemento {
   content: " ";
   width: 480px;
   grid-column: 4 / 7;
   margin-top: 15px;
   margin-left: 8px;
   height: 3px;
   background-color: #C8DCCB;
} 

.email,
.func,
.stt {
   display: flex;
   margin-top: 15px;
}
span {
   font-weight: bold;
}
</style>