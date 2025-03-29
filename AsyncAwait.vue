<script>
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const success = true; 
      if (success) {
        resolve("Data berhasil diambil!");
      } else {
        reject("Terjadi kesalahan!");
      }
    }, 5000); 
  });
}


async function getUserData() {
  try {
    console.log("Memulai pengambilan data...");
    const result = await fetchData(); 
    console.log(result); 
  } catch (error) {
    console.log("Error:", error); 
  }
}

getUserData(); 
</script>