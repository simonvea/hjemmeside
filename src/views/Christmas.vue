<template>
  <article class="christmas__container">
    <h1 class="christmas__title">Ønskeliste jul {{ year }}</h1>
    <p>Nedenfor er en liste over ting jeg ønsker meg til jul (i {{ year }}), i tilfeldig rekkefølge.</p>
    <section class="christmas__list">
      <ul>
        <li v-for="(wish, index) in wishList" v-bind:key="index">
          <a v-if="wish.link" v-bind:href="wish.link" target="_blank">{{ wish.name }}</a>
          <span v-else>{{ wish.name }}</span>
          <ul v-if="wish.info" class="christmas__list-info">
            <li>{{wish.info}}</li>
          </ul>
        </li>
      </ul>
    </section>
    <span class="christmas__updated">Sist oppdatert: {{ lastUpdated }}</span>
  </article>
</template>

<script>
export default {
  name: "christmas",
  data() {
    return {
      wishList: [
        { name: "God sovepute" },
        { name: "Barbermaskin" },
        { name: "Mocca pot" },
        { name: "Bilder/Rammer" },
        { name: "Støvsuger" },
        { name: "Tørkerullholder" },
        { name: "Kaffefilterholder" },
        { name: "Spisebordsstoler" },
        { name: "Laken/Sengetøy" }
      ],
      year: 2019,
      lastUpdated: "30.11.2019 18:40"
    };
  }
};
</script>

<style>
.christmas__container {
  min-height: 85vh;
  background-color: #b3000c;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  padding: 15px;
}

.christmas__title {
  margin: 20px;
}

.christmas__list {
  display: flex;
  justify-content: center;
  width: 360px;
  margin: 10px;
}

.christmas__list-info {
  margin-left: 15px;
}
</style>