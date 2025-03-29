<template>
  <h1 id="header">Waktu akan muncul di sini</h1>
</template>

<script>
export default {
  mounted() {
    setInterval(() => {
      document.getElementById("header").textContent = new Date().toString();
    }, 1000);
    console.info("Program Selesai");
  }
};
</script>
