<template>
  <img v-bind:src="imageUrl" alt="Vue Logo" />
  </template>
  <script setup>
  import { ref } from 'vue';
  const imageUrl = ref('https://vuejs.org/images/logo.png');
  </script>
  