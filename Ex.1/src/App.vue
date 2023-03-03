<script setup>
import { ref } from "vue";

const contador = ref(0);

function incrementar() {
  contador.value++;
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  }
}

function resetar() {
  contador.value = 0;
}
</script>

<template>
  <div>
    <div>{{ contador }}</div>

    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>
    <button @click="resetar">Resetar</button>
  </div>
</template>

<style></style>
