
<template lang="pug">
div#app
  div.top
    div.top_value
      h1 {{ hue }}%
      h1 {{ saturation }}%
      h1 {{ brightness }}%
  div.body
    div.body_bar
      //p {{ hue }}
      //VueSlider(:model="value" ref="slider")
      input(v-model="hue" max="100" min="0" type="range")
      input(v-model="saturation" max="100" min="0" type="range")
      input(v-model="brightness" max="100" min="0" type="range")
    div.body_mode
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
//import { VueColor } from 'vue-color'
//import VueSlider from 'vue-slider-component'
import 'vue-slider-component/theme/default.css'

export default {
  name: 'App',
  components: {
    HelloWorld,
    //VueSlider
  },
  data() {
    return{
      hue: 0,
      saturation: 0,
      brightness: 0
      /*
      colors: {
        hex: '#194d33',
        hsl: { h: 150, s: 0.5, l: 0.2, a: 1},
        hsv: { h: 150, s: 0.66, v: 0.30, a: 1},
        rgba: { r: 25, g: 77, b: 51, a: 1},
        a: 1
      }
      */
    }
  }
}
</script>

<style lang="sass">
#app
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  //margin-top: 60px;

  .top
    display: flex;
    flex-direction: column;
    height:  30vh;
    justify-content: flex-end;
    .top_value
      display: flex;
      justify-content: center;
  .body
    .body_bar
      display: flex;
      flex-direction: column;
</style>
