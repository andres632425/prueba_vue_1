<template>
<div>  
    <h2>Esto es un bucle que renderiza un objeto JSON</h2>
    <main>
<ul>
    <li v-for="item in items" :key="item.id">
    {{item.titulo}}
    </li>
</ul>

    </main>
</div>
</template>

<script setup>
const items= [{           id:1,
                          titulo:"Reloj Clasico", 
                          descripcion:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, sint!",
                          precio: 102.90},
                          {id:2,
                            titulo:"Reloj Moderno", 
                          descripcion:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, sint!",
                          precio: 120.90},
                          {id:3,
                          titulo:"Reloj Estilo", 
                          descripcion:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, sint!",
                          precio: 132.90}
                         ]
</script>








<style scoped>

</style>

