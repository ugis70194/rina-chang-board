<template>
  <div class="wrapper">
    <LEDArray :stateArray="face" v-for="face in faces[this.feceType]" :key="face.id" />
  </div>
  <div>
    <p> {{  }} </p>
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
      faces: faces,
      feceType: "normal",
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  margin-left: auto;
  margin-right: auto;
  display: grid;
}
</style>