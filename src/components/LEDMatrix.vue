<template>
  <div class="wrapper">
    <div class="board">
      <LEDArray :h="h" :stateArray="array" v-for="(array, h) in this.face" :key="array.id" v-on:changeState="changeState"/>
    </div>
    <div>
      <button class="btn btn-border" v-for="facetype in this.faceTypes" :key="facetype.id" @click="changeFaceType(facetype)"> {{ facetype }} </button>
    </div>
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
      faceType: "defualt",
      face: faces["defualt"]
    }
  },
  computed: {
    faceTypes() {
      return Object.keys(faces);
    },
  },
  methods: {
    changeFaceType(facetype) {
      this.faceType = facetype
      this.face = faces[facetype]
    },
    changeState(h, w) {
      this.face[h][w] ^= 1
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.board {
  margin-left: auto;
  margin-right: auto;
}

.wrapper {
  display: grid;
  grid-template-columns: 80%, 20%
}

*:before,
*:after {
  -webkit-box-sizing: inherit;
  box-sizing: inherit;
}

html {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  font-size: 62.5%;/*rem算出をしやすくするために*/
}

.btn,
a.btn,
button.btn {
  font-size: 1.6rem;
  font-weight: 700;
  line-height: 1.5;
  position: relative;
  display: inline-block;
  padding: 1rem 4rem;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  -webkit-transition: all 0.3s;
  transition: all 0.3s;
  text-align: center;
  vertical-align: middle;
  text-decoration: none;
  letter-spacing: 0.1em;
  color: #212529;
  border-radius: 0.5rem;
}

.btn-border {
  border: 2px solid #000;
  border-radius: 0;
  background: #fff;

  -webkit-transform-style: preserve-3d;

  transform-style: preserve-3d;
}

.btn-border:before {
  position: absolute;
  top: 0;
  left: 0;

  width: 5px;
  height: 100%;

  content: '';
  -webkit-transition: all .3s;
  transition: all .3s;

  background: #000;
}

.btn-border:hover {
  color: #fff;
  background: #000;
}

.btn-border:hover:before {
  background: #fff;
}


</style>