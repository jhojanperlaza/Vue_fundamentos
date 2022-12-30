<script setup>
import { ref } from "vue"
const name = "jhojan"

const counter = ref(0)

//metodo *- methods
const Increment = () =>{
    counter.value ++;
}
const Dis = () =>{
    counter.value --;
}
const Resetvalue = () =>{
    counter.value = 0;
}
</script>

<template>
    <h1> hola  {{ name.toUpperCase() }}</h1>
    <h2 :class="counter > 0 ? 'positive': 'negative'"> {{ counter }}</h2>
    <button @click="Increment">Aumentar</button>
    <button @click="Dis">Disminuir</button>
    <button @click="Resetvalue">Resetear</button>
</template>

<style>
.positive {
    color:green;
}
.negative {
    color: red;
}
</style>