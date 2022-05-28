<template>
  <div v-bind:class="{on: this.ON}">
  </div>
</template>

<script>
export default {
  name: 'LEDCell',
  props:{
    ON: Boolean
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

div {
  background-color: whitesmoke;
  height: 40px;
  border: solid 1px ;
}

.on {
  background-color: hotpink;
}
</style>
