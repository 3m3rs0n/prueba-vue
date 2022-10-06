<template>
  <div class="card">
    <div class="imagen">
      <h1>BTS</h1>
      <img
        id="imagen-card"
        alt="BTS"
        src="https://www.infobae.com/new-resizer/UdUyy2kdLkZ9TC36be5bCySm1b4=/768x512/filters:format(webp):quality(85)/cloudfront-us-east-1.images.arcpublishing.com/infobae/V4IFVN6S7NDPRD7DFFGX7ZTEDQ.png"
        width="300"
      />
      <br />
      <button v-on:click="otraFoto">Otra</button>
    </div>
    <div class="descripcion">
      Es un grupo surcoreano formado en Seúl en 2010, que debutó el 13 de junio
      de 2013 bajo la compañía Big Hit Entertainment.​Está compuesto por siete
      integrantes: Jin, Suga, J-Hope, RM, Jimin, V y Jungkook, quienes son los
      que coescriben y coproducen la mayor parte de su material discográfico.
    </div>
  </div>
</template>

<script>
let aux = 0;
export default {
  name: 'galeria',
  methods: {
    otraFoto: function (event) {
      let img = [
        'https://www.infobae.com/new-resizer/UdUyy2kdLkZ9TC36be5bCySm1b4=/768x512/filters:format(webp):quality(85)/cloudfront-us-east-1.images.arcpublishing.com/infobae/V4IFVN6S7NDPRD7DFFGX7ZTEDQ.png',
        'https://www.musicmundial.com/wp-content/uploads/2022/05/BTS-El-drama-coreano-del-grupo-que-puedes-ver-en-YouTube-768x478.jpg',
        'https://www.nacionrex.com/__export/1622933549404/sites/debate/img/2021/06/05/bts-donde-viven-2021_1_crop1622931532998.jpg_172596871.jpg',
        'https://upload.wikimedia.org/wikipedia/commons/7/73/BTS_during_a_White_House_press_conference_May_31%2C_2022_%28cropped%29.jpg',
      ];
      aux = (aux + 1) % 4;
      document.getElementById('imagen-card').src = img[aux];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  margin: 10px 0 0;
  border: 1px solid grey;
  border-radius: 10px;
}
.imagen {
  margin: 10px;
}
.descripcion {
  color: grey;
  margin: 10px;
}
</style>
