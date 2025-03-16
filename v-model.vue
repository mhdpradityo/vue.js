<template>
  <input v-model="nama" placeholder="Masukkan nama" />
  <p>Halo, {{ nama }}</p>
  </template>
  <script setup>
  import { ref } from 'vue';
  const nama = ref('');
  </script>
  