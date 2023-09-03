<template>
  <div class="base-component">
    <h1>Componente base</h1>
    <p>Este é um componente base que pode ser usado 
      como ponto de partida para outros componentes.</p>
  </div>
</template>

<script>
  export default {
    name: 'Base',
  };
</script>

<style scoped>
  .base-component {
      margin: 0 auto;
      width: 400px;
      font-size: 16px;
      text-align: center;
    }
</style>