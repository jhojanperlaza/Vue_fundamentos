<!-- Puedo tener la logica (scrips) el HTML y CSS en un mismo archivo -->
<script setup>
const name = "name Dinamico"
const styleColorred = "color:red"
const styleColorgreen = "color:green"
const arraycolores = ["red", "green", "blue", "orange"]
const activo = true
</script>

<template> <!-- Siempre se debe mostrar como minimo un template-->
  <h1>hola firma  {{ name }}</h1>  <!-- asi podemos agregar valores dinamicamente {{ valor }}-->

  <h2 v-bind:style="styleColorred">soy rojo</h2> <!-- sintaxis para agregar atributos a cualquier etiqueta-->

  <h2 :style="styleColorgreen">soy verde</h2> <!-- lo mismo de arriba pero abreviado-->

  <h2 >soy texto en mayusculas: {{ name.toUpperCase() }}</h2> <!-- Puedo utilizar metodos de js -->

  <h2> {{ arraycolores }}</h2> <!-- las interpreta como texto -->

  <h2 :style="`color: ${arraycolores[3] }`"> texto con interpolacion de js </h2>

  <h2> <!-- condicionales ternarios en vue -->
    {{ activo ? "estoy activo" : "estoy inactivo" }}
  </h2>

  <!--Condicionales en Vue-->
  <h2 v-if="activo === true">
    <span>Icono</span>
    estoy activo
  </h2>

  <p v-else-if="activo === false ">estoy inactivo</p>
  <p v-else>Estoy indeciso</p> 


</template>

<style>
h1 {
  color:blue;
}
</style>
