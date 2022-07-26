<template>
  <header class="header">
    <div class="logo">
      <img src="" alt="" />
    </div>

    <ul class="navbar">
      <li>Home</li>
      <li>Serie TV</li>
      <li>Film</li>
      <li>Nuovi e popolari</li>
      <li>La mia lista</li>
      <li>Audio e sottotitoli</li>
    </ul>

    <!-- search -->
    <form @submit.prevent="$emit('search', searchText)">
      <input
        type="text"
        placeholder="Titolo film"
        v-model="searchText"
        class="input"
      />
      <button class="button">Cerca</button>
    </form>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      searchText: "",
    };
  },
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
}
</style>
