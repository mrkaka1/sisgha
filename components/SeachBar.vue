<template v-slot:search>
  <div>
    <div class="form">
      <form action="./">
        <label class="label" for="pesquisar">Pesquisar</label>
        <input
          class="input"
          type="text"
          id="pesquisar"
          placeholder="     Procure um professor... "
        />
      </form>
    </div>
    <!-- <div class="flex items-center">
      <form action="/search" class="max-w-[480px] w-full px-4 ml-20 mt-10">
        <div class="relative">
          <input
            type="text"
            name="q"
            class="w-full border h-12 shadow p-4 rounded-full"
            placeholder="search"
          />
          <button type="submit">
            <svg
              class="text-teal-400 h-5 w-5 absolute top-3.5 right-3 fill-current"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              version="1.1"
              x="0px"
              y="0px"
              viewBox="0 0 56.966 56.966"
              style="enable-background: new 0 0 56.966 56.966"
              xml:space="preserve"
            >
              <path
                d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z"
              ></path>
            </svg>
          </button>
        </div>
      </form>
    </div> -->
  </div>
</template>
<style scoped>
.form {
  margin-left: 10%;
}
.label {
display: block;
width: 50px;
font-size: 10px;
font-weight: 600;
background-color: white;  
color: #C8DCCB;
margin-top: 60px;
margin-left: 20px;

}
.input {
height: 40px;
width: 400px;
font-weight: 550;
font-size: 0.75rem;
border-radius: 8px;
border: 2px solid #C8DCCB;
color: #C8DCCB
}
</style>
