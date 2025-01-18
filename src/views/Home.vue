<!-- src/views/Home.vue -->
<template>
    <div>
        <h1>Home</h1>
        <p>Bienvenido a la página principal.</p>
    </div>
    <HelloWorld />
</template>

<script lang="ts" setup>
import HelloWorld from '../components/HelloWorld.vue';
</script>

<style scoped>
/* Estilos específicos para la página Home */
h1 {
    color: #42b983;
}
</style>