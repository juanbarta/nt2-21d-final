<template>
  <div id="app">
    <Codificaciones />
  </div>
</template>

<script>
import Codificaciones from './components/Codificaciones.vue'


export default {
  name: 'App',
  components: {
    Codificaciones,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
