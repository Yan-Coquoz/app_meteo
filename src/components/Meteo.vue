<template>
  <div class="container">
    <h1 class="my-4">La météo du ciel</h1>
    <div class="form-groupe mb-5">
      <label for="position" class="mb-3">Entrez le nom d'une ville</label>
      <input
        id="position"
        type="text"
        class="form-control"
        v-model="requete"
        v-on:keypress="getMeteo"
      />
    </div>
    <div class="w-75 m-auto">
      <h3 class="text-center mb-4">Position : localité</h3>
      <div class="card text-center p-5 rad-15">
        <p class="text-affichage">Température : les degrés</p>
        <p class="texte-affichage">Temps : visuel</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Meteo",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
