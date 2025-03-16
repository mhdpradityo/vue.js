<script setup>
import { ref } from 'vue';
const count = ref(0);
</script>
<template>
<p>Nilai: {{ count }}</p>
<button @click="count++">Tambah</button>
</template>
