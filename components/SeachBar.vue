<template v-slot:search>
  <div>
    <div class="form">
      <form action="./">
        <label id="label" class="label" for="pesquisar">Pesquisar</label>
        <IconsIconSearch class="icon"/>
        <input
          class="input"
          type="text"
          id="pesquisar"
          placeholder="Digite aqui "
        />
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const searchTerm = ref('');
const filteredItems = ref([]);

const filterItems = () => {
  filteredItems.value = items.value.filter(item =>
    item.name.toLowerCase().includes(searchTerm.value.toLowerCase())
  );
};
</script>
<style scoped>
.form {
  display: flex;
  margin-left: 150px;
  margin-top: 90px;
  position: relative;
  align-items: center;
}
.label {
  display: inline-block;
  padding: 5px;
  width: auto;
  margin-top: -13px;
  font-size: 10px;
  font-weight: 600;
  border: 1px solid white;
  background-color: white;
  color: #c8dccb;
  position: absolute;
}
input {
  height: 40px;
  width: 400px;
  font-weight: 550;
  font-size: 0.75rem;
  border-radius: 8px;
  border: 2px solid #c8dccb;
  transition: border-color 0.3s;
  padding: 16px;
  font-size: 12px;
  flex: 1;
}

input::placeholder {
  padding: 4px;
  margin: 5px;
}

input:focus {
  outline: none;
  border-color: #00D047;
}

.icon {
  position: absolute;
  left: 370px;
  top: 20px;
  transform: translateY(-50%);
  fill: #c8dccb;
  transition: fill 0.3s;
  cursor: pointer;
}

.form:focus-within label {
  color: #00D047;
  transition: 0.3s;
}

.form:focus-within .icon{
  fill: #00D047;
}
</style>
