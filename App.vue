<template>
  <p v-if="loggedIn">Selamat datang, user!</p>
  <p v-else>Silakan login</p>
  <button @click="loggedIn = !loggedIn">Tombol Login</button>
  </template>
  <script setup>
  import { ref } from 'vue';
  const loggedIn = ref(false);
  </script>
  