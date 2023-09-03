<template>
  <h2>Coloque seu nome e sua nota</h2>
  <input v-model="nome" type="text">
  <input v-model="numero" type="number">
  <button v-on:click="salvarnota"></button>


  
</template>

<script>
  //import Base from './components/Base.vue'
  import Base from './components/componente.veu'
  export default {
    components: {
     nome,
     nota,
    },
  };
</script>

<style scoped>

</style>
