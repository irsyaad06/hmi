<script setup>
// Jika Anda menggunakan Vue Router, Anda bisa mengganti ini dengan <RouterView />
import Home from './views/HomeView.vue'
</script>

<template>
  <main class="app-container">
    <Home />
  </main>
</template>

<style>
*, *::before, *::after {
  box-sizing: border-box;
}

#app {
  width: 100%;
  min-height: 100vh;
  margin: 0;
  padding: 0;
  max-width: none; /* Menghapus max-width bawaan Vue */
  display: block;  /* Menghapus flex/grid bawaan #app di Vue */
}

.app-container {
  width: 100%;
  min-height: 100vh;
}
</style>