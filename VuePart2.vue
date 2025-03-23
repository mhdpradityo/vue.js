<template>
  <div>
    <h2>List Rendering</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ index + 1 }}.{{ item }}
      </li>
    </ul>
    <h2>Computed Properties</h2>
    <p>Jumlah Item: {{ itemCount }}</p>

    <h2>Watchers</h2>
    <p>Input: <input v-model="inputText" /></p>
    <p>Hasil:{{ inputText }}</p>

    <h2>Tempalte Ref&Lifecycle Hook</h2>
    <p ref="paragraphRef">
      Ini adalah paragraf yang akan diakses di lifecycle hook
    </p>
  </div>
</template>

<script>
import { ref, computed, watch, onMounted } from "vue";
export default {
  setup() {
    const items = ref(["Ban", "Oli", "Stang", "Rem"]);
    const itemCount = computed(() => items.value.length);
    const inputText = ref("");
    watch(inputText, (newValue, oldValue) => {
      console.log('Input berubah dari"${oldValue}" menjadi "${newValue}""');
    });

    const paragraphRef = ref(null);
    onMounted(() => {
      console.log("Elemen paragraf:", paragraphRef.value);
    });
    return { items, itemCount, inputText };
  },
};
</script>
