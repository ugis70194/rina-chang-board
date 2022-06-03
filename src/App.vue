<template>
  <h1> Rina chang board </h1>
  <div class="wrapper">
    <div class="menu"> fece select </div>
  </div>
  <ul class="wrapper">
    <input placeholder="facename"/>
    <button > save </button>
  </ul>
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
}

.wrapper {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
}

.menu {
  width: 60%;
  height: 2rem;
  font-size: 1.5rem;
  background-color: black;
  color: white;
  justify-self: center;
}

.menu:hover {
  background-color: gray;
}

ul input {
  height: 2rem;
  width: 45%;
  font-size: 1.5rem;
}

ul button {
  height: 2rem;
  width: 15%;
  font-size: 1.5rem;
}


</style>
