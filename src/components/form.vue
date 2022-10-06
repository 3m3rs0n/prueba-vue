<template>
  <div>
    <h5>Ingresa tu nombre:</h5>
    <input id="nombre" type="text" />
    <button v-on:click="mandarNombre">Enviar</button>
    <h5 id="salida"></h5>
  </div>
</template>

<script>
export default {
  name: 'Nao',
  methods: {
    mandarNombre: function (event) {
      var nombre = document.getElementById('nombre').value;
      document.getElementById('salida').innerText =
        'Bienvenido, ' + nombre + ' !';
    },
  },
};
</script>

<style>
input {
  border-radius: 5px 1px solid #979797;
}
button {
  margin: 5px;
  background-color: #42b983;
  border: 1px solid white;
  padding: 5px;
  color: white;
}
* {
  font-weight: 100;
}
</style>
