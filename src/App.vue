<template>
  <div>
    <h1 :class="titular">Esto es un archivo principal para {{ valor }}</h1>
    <button @:click="cambiar">{{ mensaje }}</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const valor = "El Bootcamp";
let titular = ref("oscuro");
let mensaje = ref("CLARO");
const cambiar = () => {
  if (titular.value == "oscuro") {
    titular.value = "claro";
    mensaje.value = "OSCURO";
  } else {
    titular.value = "oscuro";
    mensaje.value = "CLARO";
  }
};
</script>

<style scoped>
.oscuro {
  background-color: blue;
  color: azure;
}

.claro {
  background-color: rgb(190, 237, 172);
  color: rgb(43, 77, 77);
}
</style>
