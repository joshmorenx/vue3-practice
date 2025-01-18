<!-- src/App.vue -->
<template>
  <div>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view />
  </div>
</template>

<script setup>
</script>

<style>
nav {
  background-color: #42b983;
  padding: 10px;
}

nav a {
  color: white;
  margin-right: 10px;
  text-decoration: none;
}
</style>
