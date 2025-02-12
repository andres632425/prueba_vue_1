<template>
  <div>
    <h1 :class="titulo">Esto es un archivo principal para {{ proyecto }}</h1>
    <section v-bind:class="seccion">
      <h3>Primer Item</h3>
      <TitularEstilos />
    </section>

    <section v-bind:class="seccion">
      <h3>Segundo Item</h3>
      <JsonBucle />
    </section>

    <section v-bind:class="seccion">
      <h3>Tercer Item</h3>
      <h5>Este es el parent</h5>
      <PropsEmits :valorPasado1="tipoCurso" :duracionCursoMeses="duracionCursoMeses" @respuesta="cambiarCurso" />
    </section>

    <section v-bind:class="seccion">
      <h3>Cuarto Item</h3>
      <ProvideInjection />
    </section>

    <section v-bind:class="seccion">
      <h3>Quinto Item</h3>
      <FechtApi />
    </section>
  </div>
</template>
<script setup>
import TitularEstilos from "./components/TitularEstilos.vue";
import JsonBucle from "./components/JsonBucle.vue";
import PropsEmits from "./components/PropsEmits.vue";
import ProvideInjection from "./components/ProvideInjection.vue";
import FechtApi from "./components/FechtApi.vue";

import { ref, provide } from "vue";

// Data de <TitularEstilos/>
let proyecto = ref("vue");
let titulo = ref("estilo");
let seccion = "seccion";

// Data de  <PropsEmits/>
let tipoCurso = ref("Bootcamp Fullstack");
let duracionCursoMeses = ref(8);

const cambiarCurso = (uno, dos) => {
  tipoCurso.value = uno;
  duracionCursoMeses.value = dos;
};
// Data de  <ProvideInjection/>
const stackFullstack = ref("Frontend, Backend, API-Rest");
provide("tipoStack", stackFullstack);
</script>

<style scoped>
.estilo {
  font-size: 3rem;
  color: blue;
  margin-bottom: 3rem;
}
.seccion {
  width: 80%;
  padding: 2rem;
  border: 0.4rem solid brown;
  color: rgb(9, 1, 1);
  background-color: aqua;
  margin: 3rem;
}
</style>
