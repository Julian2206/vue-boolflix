<template>
  <div class="main">
    <FilmList :films="films" />
  </div>
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

<style lang="scss" scoped></style>
