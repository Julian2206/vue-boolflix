<template>
  <div class="container">
    <h2>Film</h2>
    <ul>
      <li v-for="(film, index) in films" :key="index" class="item"></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FilmList",
  components: {},
  props: {
    films: Array,
  },
};
</script>

<style></style>
