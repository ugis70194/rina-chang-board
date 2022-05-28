<template>
  <div class="wrapper">
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
    <LEDCell v-bind:ON="true" />
  </div>
</template>

<script>
import LEDCell from './LEDCell.vue'

export default {
  name: 'LEDArray',
  components: {
    LEDCell
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  margin-left: auto;
  margin-right: auto;
  display: grid;
  grid-template-columns: 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px 60px;
  width: 960px;
}
</style>