<template>
  <div class="wrapper">
    <LEDCell :ON="state" v-for="state in stateArray" :key="state.id" />
  </div>
</template>

<script>
import LEDCell from './LEDCell.vue'

export default {
  name: 'LEDArray',
  components: {
    LEDCell
  },
  props: {
    stateArray: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  margin-left: auto;
  margin-right: auto;
  display: grid;
  grid-template-columns: 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px 40px;
}
</style>