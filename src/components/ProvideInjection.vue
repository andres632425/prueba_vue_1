<template>
  <div>
    <h2>Pase de datos por provide e inyection </h2>
    <h5>Este es el child provide/injection</h5>
    <p>El stack del Bootcamp de fullstack es {{todoStack}} </p>
 <button @click="ordenStack">Cambiar Stack</button>
  </div>
</template>

<script setup>
import { inject } from "vue";

const todoStack=inject('tipoStack');
const ordenStack=()=>{

todoStack.value="API-Rest, Backend, Frontend"

}
</script>

<style scoped>

</style>
