<template>
  <div class="div">
    <h1>Janet she be the Queen</h1>
    <h1>Número de vezes clicadas: {{ count }}</h1>
    <button @click="onClick">Clica no pae</button>
    <button @click="clean">Clean</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const count = ref(0)
const onClick = () => {
  count.value = count.value + 1
}
const clean = () => {
  count.value = 0
}
</script>

<style lang="css">
.div {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
button {
  width: 100px;
}
</style>
