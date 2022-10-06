<template>
  <div id="app">
    <img
      alt="Vue logo"
      src="https://github.com/MicaelaGordillo/TrabajoDeClase_06102022/blob/main/images/blacklist.jpg?raw=true"
    />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Btn>Soy pepinillo RICK !!!!</Btn>
    <Nao />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import * as Btn from './components/ButtonTest.vue';
import ColorButton from './components/colorButton.vue';
import Nao from './components/form.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Btn,
    ColorButton,
    Nao,
  },
};
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
