//Exercício operações matemáticas

<script>
export default {
  data() {
    return {
      numeroParaDobrar: 0,
      numeroSomar1:0,
      numeroSomar2:0,
    }
  },
  methods: {
    dobrarNumero() {
      return this.numeroParaDobrar * 2
    },
    somar() {
      return this.numeroSomar1 + this.numeroSomar2
    }
  }
}
</script>

<template>
  <div class="all">
    <div class="dobroNmr">
      <h2>Dobro do número</h2>
      <input type="number" name="" id="" placeholder="Digite um número" v-model="numeroParaDobrar" /> <br />
      {{ dobrarNumero() }}
    </div>
    <div class="somaNmr">
      <h2>Soma de números</h2>
      <input type="number" v-model="numeroSomar1">
      <input type="number" v-model="numeroSomar2"> <br>
      {{ somar() }}
      <div v-if="(somar()%2 == 0)">A soma é par</div>
      <div class="somaMaiorQue10" v-if="(somar() > 10)">A soma é maior que 10</div>
    </div>
  </div>
</template>

<style scoped>

.dobroNmr{
  margin-bottom: 20px;
} 

.somaMaiorQue10 {
  color: red;
}

</style>
