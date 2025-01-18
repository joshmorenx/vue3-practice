<script setup lang="ts">
import { ref } from 'vue'
import { User } from '../interfaces/User';

// Estados reactivos
const users = ref<User[]>([]);
const loading = ref(false);

// Función para consumir la API
const fetchUsers = async () => {
  loading.value = true;
  const response = await fetch('https://jsonplaceholder.typicode.com/users');
  users.value = await response.json();
  loading.value = false;
};
</script>

<template>
  <div> 
    <h1>Lista de Usuarios</h1>
    <button @click="fetchUsers">Cargar Usuarios</button>
    <p v-if="loading">Cargando...</p>
    <ul>
      <li v-for="user in users" :key="user.id">{{ user.name }}</li>
    </ul>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}

button {
  margin: 10px 0;
  padding: 8px 12px;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background: #0056b3;
}
</style>
