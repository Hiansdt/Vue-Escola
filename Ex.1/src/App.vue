//Exercício contador

<script setup>
import { ref } from "vue";

const contador = ref(0);
const definir = ref();

function incrementar() {
  contador.value++;
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  } else {
    alert("O contador não pode ir abaixo de 0!")
  }
}

function resetar() {
  contador.value = 0;
}

function alterarValor() {
  contador.value = definir.value;
  definir.value = Number;
}
</script>

<template>
  <div>
    <div>{{ contador }}</div>
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>
    <button @click="resetar">Resetar</button> <br />
    <input
      type="number"
      v-model="definir"
      placeholder="Definir valor do contador"
    />
    <button @click="alterarValor()">Enviar</button>
    <div class="verde" v-if="contador > 10">O contador está acima de 10</div>
    <div class="vermelho" v-if="contador < 10">
      O contador está abaixo de 10
    </div>
  </div>
</template>

<style scoped>
.verde {
  color: green;
  font-weight: bold;
}

.vermelho {
  color: red;
  font-weight: bold;
}
</style>
