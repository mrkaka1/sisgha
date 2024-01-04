<template>
  <div>
    <div class="initmodal2">
      <IconsIconBeforeDays class="iconb"/>
      <h1 class="teste">teste</h1>
      <IconsIconAfterDays class="iconA"/>
   </div>
   <div class="contentModal">
      <HoursMarkup />
   </div>
  </div>
</template>

<style>
.initmodal2, 
.contentModal {
   display: flex;
   align-items: center;
}

.iconb,
.iconA, 
.teste {
   display: flex;
   flex: 1 1 auto;  
   margin-top: 8%;
}

.teste {
   justify-content:  center;
}

.iconA {
   justify-content: end;
}

.iconA, 
.iconb {
   cursor: pointer;
}
</style>


<!-- 
<section class="dispo none">
            <ul class="dias">
               <li class="dia1">Seg</li>
               <li class="dia2">Ter</li>
               <li class="dia3">Qua</li>
               <li class="dia4">Qui</li>
               <li class="dia5">Sex</li>
               <li class="dia6">Sáb</li>
            </ul>
      </section>

 -->