//Exercício pessoas e nomes
<script setup>
const nome = 'Vinícius'
const idade = 16

function inverterTexto(texto) {
  return texto.split('').reverse().join('')
}
</script>

<template>
  <div class="all">
    <div class="info">
      <div class="nome">Nome: {{ nome }}</div>
      <div class="idade">Idade: {{ idade }} anos</div>
    </div>
    <div class="outro">
      <div>Anos para completar 50: {{ 50 - idade }} anos</div>
      <div>O nome tem {{ nome.split('').length }} letras</div>
      <div>O nome invertido é {{ inverterTexto(nome) }}</div>
    </div>
  </div>
</template>

<style scoped>
.info {
  background-color: black;
  color: white;
  border-bottom: 1px solid white;
}
.outro {
  background-color: black;
  color: white;
}
</style>
