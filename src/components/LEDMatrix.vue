<template>
  <div class="board">
    <LEDArray :h="h" :stateArray="array" v-for="(array, h) in this.face" :key="array.id" v-on:changeState="changeState"/>
  </div>
  <div>
    <button v-for="facetype in this.faceTypes" :key="facetype.id" @click="changeFaceType(facetype)"> {{ facetype }} </button>
  </div>
</template>

<script>
import LEDArray from './LEDArray.vue'
import faces from '../assets/faces.json'

export default {
  name: 'LEDMatrix',
  components: {
    LEDArray
  },
  data (){
    return {
      faceType: "defualt",
      face: faces["defualt"]
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
      this.face = faces[facetype]
    },
    changeState(h, w) {
      console.log(h, w)
      this.face[h][w] ^= 1
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.board {
  margin-left: auto;
  margin-right: auto;
  display: grid;
}
</style>