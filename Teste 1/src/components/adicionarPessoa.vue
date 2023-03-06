<script>
    export default {
        data() {
            return {
                novoNome: Text,
            }
        }
    }
</script>

<template>
  <form action="">
    <input type="text" class="add" v-model="novoNome"/>
    <input type="number" class="add" />
    <input type="text" class="add" />
  </form>
</template>

<style scoped></style>
