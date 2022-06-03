<template>
  <div v-bind:class="{on: this.state}" @click="changeState">
  </div>
</template>

<script>
export default {
  name: 'LEDCell',
  props:{
    state: Number,
    h: Number,
    w: Number,
  },
  methods: {
    changeState() {
      this.$emit('changeState', this.h, this.w)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

div {
  background-color: whitesmoke;
  height: 3rem;
  border: solid 1px ;
}

.on {
  background-color: hotpink;
}
</style>
