<template>
  <div class="container">
    <h1 class="my-4">La météo du ciel</h1>
    <div class="form-groupe mb-5">
      <label for="position" class="mb-3">Entrez le nom d'une ville</label>
      <input
        id="position"
        type="text"
        class="form-control"
        v-model="inputReq"
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
import axios from "axios";
export default {
  name: "Meteo",
  data() {
    return {
      inputReq: "",
      temps: undefined,
      apiKey: "67f7b3cd740899b4fbe49b4494d34b83",
      base_url: "https://api.openweathermap.org/data/2.5/weather?",
    };
  },
  methods: {
    getMeteo(evt) {
      // lancement de la inputReq avec la touche enter
      if (evt.key === "Enter") {
        console.log(this.apikey);
        axios
          .get(
            `${this.base_url}q=${this.inputReq}&units=metric&appid=${this.apiKey}&lang=fr`,
          )
          .then((response) => {
            this.temps = response.data;
          });
        // vide l'input
        this.inputReq = "";
      }
    },
  },
};
</script>

<style></style>
