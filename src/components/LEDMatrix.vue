<template>
  <div class="board">
    <LEDArray :h="h" :stateArray="array" v-for="(array, h) in this.faceData" :key="array.id" v-on:changeState="changeState"/>
  </div>
</template>

<script>
import LEDArray from './LEDArray.vue'

export default {
  name: 'LEDMatrix',
  components: {
    LEDArray
  },
  props: {
    faceData: Object
  },
  methods: {
    changeState(h, w) {
      this.$emit('changeState', h, w)
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