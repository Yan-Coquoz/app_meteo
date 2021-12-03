<template>
  <div id="app">
    <Meteo />
  </div>
</template>

<script>
import Meteo from "./components/Meteo.vue";

export default {
  name: "App",
  components: {
    Meteo,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Fuzzy+Bubbles&family=Irish+Grover&display=swap");

body {
  background: #ff4e50; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #f9d423,
    #ff4e50
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #f9d423,
    #ff4e50
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  font-family: "Fuzzy Bubbles", cursive;
}
</style>
