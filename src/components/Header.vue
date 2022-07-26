<template>
  <div class="header">
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

    <form @submit.prevent="$emit('search', searchText)">
      <input
        type="text"
        placeholder="Titolo film"
        v-model="searchText"
        class="input"
      />
      <button class="button">Cerca</button>
    </form>
  </div>
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

<style></style>
