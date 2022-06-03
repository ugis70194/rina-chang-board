<template>
  <h1> Rina chang board </h1>
  <li>
    <ul>a</ul>
    <ul>b</ul>
  </li>
  <LEDMatrix :faceData="this.faceData" v-on:changeState="changeState"/>
</template>

<script>
import LEDMatrix from './components/LEDMatrix.vue'
import faces from './assets/faces.json'

export default {
  name: 'App',
  components: {
    LEDMatrix
  },
  data (){
    return {
      faceType: "defualt",
      faceData: faces["defualt"]
    }
  },
  computed: {
    faceTypes() {
      return Object.keys(faces);
    },
  },
  methods: {
    changeFaceType(facetype) {
      this.faceType = facetype
      this.faceData = faces[facetype]
    },
    changeState(h, w) {
      this.faceData[h][w] ^= 1
    }
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
