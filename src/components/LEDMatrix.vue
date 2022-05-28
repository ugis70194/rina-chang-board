<template>
  <div class="wrapper">
    <LEDArray :stateArray="faces[this.feceType][0]"/>
    <LEDArray :stateArray="faces[this.feceType][1]"/>
    <LEDArray :stateArray="faces[this.feceType][2]"/>
    <LEDArray :stateArray="faces[this.feceType][3]"/>
    <LEDArray :stateArray="faces[this.feceType][4]"/>
    <LEDArray :stateArray="faces[this.feceType][5]"/>
    <LEDArray :stateArray="faces[this.feceType][6]"/>
    <LEDArray :stateArray="faces[this.feceType][7]"/>
    <LEDArray :stateArray="faces[this.feceType][8]"/>
    <LEDArray :stateArray="faces[this.feceType][9]"/>
    <LEDArray :stateArray="faces[this.feceType][10]"/>
    <LEDArray :stateArray="faces[this.feceType][11]"/>
    <LEDArray :stateArray="faces[this.feceType][12]"/>
    <LEDArray :stateArray="faces[this.feceType][13]"/>
    <LEDArray :stateArray="faces[this.feceType][14]"/>
    <LEDArray :stateArray="faces[this.feceType][15]"/>
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