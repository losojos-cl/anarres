<script setup> 
const name = "anarres";
const styleColor = "color: blue";
const arrayColores = ["red", "blue", "green"];
const activo = false;
</script>

<template>
<h1>Welcome to {{ name.toUpperCase() }}</h1>
<h2 :style="`color: ${arrayColores[1]}`">hombre azul</h2>
<h2>
  {{ activo ? "activo" : "inactivo" }}
</h2>
</template>

<style>
h1 {
  color: red;
}
</style>