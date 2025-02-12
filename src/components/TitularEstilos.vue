<template>
  <div>
    <h2 :class="titular">Cambio de estilos oscuro/claro por {{ valor }}</h2>
    <button @:click="cambiar">{{ mensaje }}</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const valor = "evento click";
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
