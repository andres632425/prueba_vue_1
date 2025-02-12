<template>
  <div>
    <h2>Pase de datos por props y emits </h2>
    <h5>Este es el child</h5>
    <p>El curso es {{valorPasado1}} y su duracion es de {{duracionCursoMeses}} meses</p>
    <button  @click="cambiar">Cambiar Curso</button>
  </div>
</template>
<script setup>
const emit=defineEmits('respuesta');
const cambiar=()=>{
      emit('respuesta','Bootcamp Frontend',5)

}

const props=defineProps({
    valorPasado1:String,
    duracionCursoMeses:Number
})


</script>

<style scoped>

</style>