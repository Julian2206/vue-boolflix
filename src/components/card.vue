<template>
  <div class="card">
    <img
      :src="`https://image.tmdb.org/t/p/w342/${info.poster_path}`"
      :alt="`${info.original_title || info.original_name}`"
    />

    <div class="card_hover">
      <h4>{{ info.title || info.name }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    info: Object,
  },
  data() {
    return {
      flags: ["it", "en"],
    };
  },
  computed: {
    starRating() {
      return Math.ceil(this.info.vote_average / 2);
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  text-align: center;
  overflow-y: hidden;
}
</style>
