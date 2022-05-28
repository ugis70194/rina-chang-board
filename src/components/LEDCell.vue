<template>
  <div v-bind:class="{on: ON}">
    cell
  </div>
</template>

<script>
export default {
  name: 'LEDCell',
  props: {
    ON: Boolean
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

div {
  background-color: lightgray;
  height: 60px;
}

.on {
  background-color: hotpink;
}
</style>
