<script setup>
const name = "jhojan"
const ObjetoFruta = 
    {
        name: "Manzana",
        price: "$1.00",
        description: "Una manzana",
        stock: 0,
    }

</script>

<template>
    <h1> hola  {{ name.toUpperCase() }}</h1>
    <h2> {{ ObjetoFruta }}</h2>
    <ul>
        <li v-for="(value, key, index) in ObjetoFruta" :key="value">
            {{ index }} - {{ key }} - {{ value }}
        </li>
    </ul>
</template>