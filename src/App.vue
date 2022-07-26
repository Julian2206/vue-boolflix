<template>
  <div id="app">
    <Header @search="searching" />
    <Main :films="films" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import axios from "axios";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      films: [],
    };
  },
  methods: {
    searching(needle) {
      //movie search
      axios
        .get("https://api.themoviedb.org/3/search/movie", {
          params: {
            api_key: "ce232ff9f4f00fd292cb08924ac4c7d2",
            query: needle,
            language: "it-IT",
          },
        })
        .then((response) => {
          console.log(response.data.results);
          this.films = response.data.results;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<style lang="scss"></style>
