<template>
  <div class="wrapper">
    <LEDCell :h="this.h" :w="w" :state="state" v-for="(state, w) in stateArray" :key="state.id" v-on:changeState="changeState" />
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
    stateArray: Array,
    h: Number
  },
  methods: {
    changeState(h, w) {
      this.$emit('changeState', h, w)
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  margin-left: auto;
  margin-right: auto;
  display: grid;
  grid-template-columns: 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem 3rem;
}
</style>