<template>
  <UserAuth />
  <ul>
    <li v-for="bicicleta in bicicletas" :key="bicicleta.id">
      <button @click="inspeccionarBicicleta(bicicleta.id)">Eliminar</button>
      {{ bicicleta.id }} - {{ bicicleta.marca }} - {{ bicicleta.modelo }}
    </li>
  </ul>
</template>

<script>
type Bicicleta = {
  id: number,
  marca: string,
  modelo: string,
  color: string,
  precio: number,
  imagen: string,
  descripcion: string,
};
</script>

<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";

const bicicletas: Ref<Bicicleta[]> = ref([]);

function fetchBicicletas() {
  fetch("http://localhost:3000/bicicletas")
    .then((response) => {
      if (response.ok) {
        return response.json();
      }
      throw new Error(response.statusText);
    })
    .then((json) => {
      bicicletas.value = json;
    })
    .catch((error) => {
      console.log("Error: ", error);
    });
}
fetchBicicletas();

function inspeccionarBicicleta(id: number) {
  const bicicleta = bicicletas.value.find((bici) => bici.id === id);
}
</script>

<style></style>
