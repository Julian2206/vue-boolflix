<template>
  <div class="container">
    <h2>Film</h2>
    <ul>
      <li v-for="(film, index) in films" :key="index" class="item">
        <Card :info="film" />
      </li>
    </ul>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "FilmList",
  components: {
    Card,
  },
  props: {
    films: Array,
  },
};
</script>

<style></style>
