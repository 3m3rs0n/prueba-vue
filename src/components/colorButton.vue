<template>
  <button v-on:click="setColor"></button>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  methods: {
    setColor: function (event) {
      const c = document.getElementById('fondo');
      console.log(c);
      c.addEventListener('load', cambiarColor());
    },

    cambiarColor: function (event) {
      const ColorsArray = [
        '#557588',
        '#4C8AB9',
        '#84C0F7',
        '#D0E9FB',
        '#91ce7b',
        'white',
      ];
      const fondo = document.getElementById('fondo');
      var r = Math.floor(Math.random() * 6);
      fondo.style.backgroundColor = ColorsArray[r];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
