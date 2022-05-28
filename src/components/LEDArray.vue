<template>
  <div class="wrapper">
    <LEDCell :ON="stateArray[0]" />
    <LEDCell :ON="stateArray[1]" />
    <LEDCell :ON="stateArray[2]" />
    <LEDCell :ON="stateArray[3]" />
    <LEDCell :ON="stateArray[4]" />
    <LEDCell :ON="stateArray[5]" />
    <LEDCell :ON="stateArray[6]" />
    <LEDCell :ON="stateArray[7]" />
    <LEDCell :ON="stateArray[8]" />
    <LEDCell :ON="stateArray[9]" />
    <LEDCell :ON="stateArray[10]" />
    <LEDCell :ON="stateArray[11]" />
    <LEDCell :ON="stateArray[12]" />
    <LEDCell :ON="stateArray[13]" />
    <LEDCell :ON="stateArray[14]" />
    <LEDCell :ON="stateArray[15]" />
    <LEDCell :ON="stateArray[16]" />
    <LEDCell :ON="stateArray[17]" />
    <LEDCell :ON="stateArray[18]" />
    <LEDCell :ON="stateArray[19]" />
    <LEDCell :ON="stateArray[20]" />
    <LEDCell :ON="stateArray[21]" />
    <LEDCell :ON="stateArray[22]" />
    <LEDCell :ON="stateArray[23]" />
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