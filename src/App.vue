<script setup>
const name = "anarres";
const styleColor = "color: blue";
const arrayColores = ["red", "blue", "green"];
const activo = false;
const arrayNumeros = [13, 62, 73, 14, 95];
const arrayPersonas = [
  { nombre: "Ana", edad: 30, residencia: "Madrid", id: 1},
  { nombre: "Juan", edad: 25, residencia: "Barcelona", id: 2 },
  { nombre: "Pedro", edad: 40, residencia: "Valencia", id: 3 },
  { nombre: "María", edad: 35, residencia: "Sevilla", id: 4 },
  { nombre: "Luis", edad: 28, residencia: "Bilbao", id: 5 },
];
const objetoPersona = {
  nombre: "Ana",
  edad: 30,
  residencia: "Madrid",
};
</script>

<template>
  <h1>Welcome to {{ name.toUpperCase() }}</h1>
  <h2 :style="`color: ${arrayColores[1]}`">hombre azul</h2>
  <h2>
    {{ activo ? "disponible" : "no disponible" }}
  </h2>
  <h3 v-if="activo === true">Este es un mensaje activo</h3>
  <h3 v-if="activo === false">Este es un mensaje inactivo</h3>
  <h4>recorrer array</h4>
  <ul>
    <li :style="`color: ${arrayColores[2]}`"  v-for="(numero, index) in arrayNumeros" :key="index">
      {{ index }} - {{ numero }}
    </li>
  </ul>
  <h4>recorrer array de objetos</h4>
  <ul>
    <li :style="`color: ${arrayColores[1]}`"  v-for="(persona, index) in arrayPersonas" :key="persona.id">
      {{ persona.nombre }} ({{ persona.edad }} años, de {{ persona.residencia }})
    </li>
  </ul>
  <h4>recorrer objeto</h4>
  <ul>
    <li :style="`color: ${arrayColores[0]}`" v-for="(value, propiedad) in objetoPersona" :key="value">
      {{ propiedad }}: {{ value }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>