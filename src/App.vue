<template>
  <h1> Rina chang board </h1>
  <LEDMatrix/>
</template>

<script>
import LEDMatrix from './components/LEDMatrix.vue'

export default {
  name: 'App',
  components: {
    LEDMatrix
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
