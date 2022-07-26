<template>
  <main class="main">
    <FilmList :films="films" />
  </main>
</template>

<script>
import FilmList from "./FilmsList.vue";

export default {
  name: "Main",
  components: {
    FilmList,
  },
  props: {
    films: Array,
  },
};
</script>

<style lang="scss" scoped>
main {
  background-color: lightgrey;
}
</style>
