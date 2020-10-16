
<template lang="pug">
div#app
  div.top
    h1 25%
    h1 55%
    h1 78%
    picker(v-model="colors")
  div#body
    div#bar
     //p {{ colors }}
     picker(v-model="colors")
    div#mode
  //img(alt="Vue logo" src="./assets/logo.png")
  //HelloWorld(msg="Welcome to Your Vue.js App" )
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { VueColor } from 'vue-color'

export default {
  name: 'App',
  components: {
    HelloWorld,
    picker: VueColor
  },
  data() {
    return{
      colors: {
        hex: '#194d33',
        hsl: { h: 150, s: 0.5, l: 0.2, a: 1},
        hsv: { h: 150, s: 0.66, v: 0.30, a: 1},
        rgba: { r: 25, g: 77, b: 51, a: 1},
        a: 1
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
