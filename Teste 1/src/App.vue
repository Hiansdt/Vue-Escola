<script setup>
import { ref } from 'vue'
//import novoNome from './components/adicionarPessoa.vue';

class pessoa {
  constructor(nome, idade, profissao) {
    this.nome = nome
    this.idade = idade
    this.profissao = profissao
  }
}
const pessoa1 = new pessoa('Vini', 16, 'Estudante')
const pessoa2 = new pessoa('Enzo', 16, 'Estudante')
const pessoa3 = new pessoa('Lucas', 17, 'Estudante')

const todos = ref([pessoa1, pessoa2, pessoa3])

const pessoaAtual = ref(todos.value[0])

function prox() {
  if (todos.value.indexOf(pessoaAtual.value) !== todos.value.length - 1) {
    pessoaAtual.value = todos.value[todos.value.indexOf(pessoaAtual.value) + 1]
  } else {
    pessoaAtual.value = todos.value[0]
  }
}

function ant() {
  if (todos.value.indexOf(pessoaAtual.value) !== 0) {
    pessoaAtual.value = todos.value[todos.value.indexOf(pessoaAtual.value) - 1]
  } else {
    pessoaAtual.value = todos.value[todos.value.length - 1]
  }
}
</script>

<template>
  <div class="all">
    <div class="info">
      <div class="infoPeca">{{ pessoaAtual.nome }}</div>
      <div class="infoPeca">{{ pessoaAtual.idade }}</div>
      <div class="infoPeca">{{ pessoaAtual.profissao }}</div>
    </div>

    <button class="btn" @click="ant">Anterior</button>
    <button class="btn" @click="prox">Próximo</button>
    <button class="btn add">+</button>

    //<div>{{ novoNome }}</div>
  </div>
</template>

<style scoped>

  .info{
    background-color: black;
    color: white;
    border-radius: 10px;
  }

  .info>div{
    border-bottom: 1px solid white;
  }
  .btn {
    background-color: grey;
    color: aliceblue;
  }

</style>
