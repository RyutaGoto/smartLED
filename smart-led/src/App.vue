
<template lang="pug">
div#app
  div.top(:style="styleVariables")
    div.top_value
      h1 {{ hue }}%
      h1 {{ saturation }}%
      h1 {{ brightness }}%
  div.body
    div.body_bar
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
      hue: 50,
      saturation: 50,
      brightness: 50
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
  },
  computed: {
    styleVariables() {
      return {
        '--hue': this.hue,
        '--saturation': this.saturation,
        '--brightness': this.brightness
      };
    },
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
    --hue: 50%; //デフォルト値
    --saturation: 50% //デフォルト値
    --brightness: 50%  //デフォルト値
    //background: hsl(var(--hue), var(--saturation), var(--brightness));
    background-color: hsl(100, 100%, 100%);
    display: flex;
    flex-direction: column;
    height:  30vh;
    justify-content: flex-end;
    .top_value
      display: flex;
      justify-content: center;
  .body
    //background-color: hsl(100, 100%, 100%);
    //background-color: #000;
    margin: 20% 0 0 0;
    .body_bar
      display: flex;
      flex-direction: column;
</style>
