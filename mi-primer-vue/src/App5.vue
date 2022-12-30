<script setup>
const name = "jhojan"
//metodo *- methods
const handleClicks = () =>{
    console.log("me diste click")
}
</script>

<template>
    <h1> hola  {{ name.toUpperCase() }}</h1>
    <button v-on:click="handleClicks">Activame1</button>
    <button @click="handleClicks">Activame2</button> <!--forma abreviada-->
</template>
