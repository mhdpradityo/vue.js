<script>
let fetchData = new Promise((resolve, reject) => {
  setTimeout(() => {
    let success = True;
    if (success) {
      resolve("Data berhasil diambil!");
    } else {
      reject("Terjadi kesalahan!");
    }
  }, 5000);
});
fetchData
.then(result => {
  console.log(result); 
})
.catch(error => {
    console.log(error);
  });
</script>