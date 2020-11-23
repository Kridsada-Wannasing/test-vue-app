<template>
  <v-container class="text-center">
    <v-row>
      <v-col><h2>Film List</h2></v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-divider></v-divider>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4" v-for="(film, i) in filmLists" :key="i">
        <div
          style="background-color: gray; width: 190px; height:190px;"
          class="d-flex align-end"
        >
          <div style="background-color: black; color:white; width:100%;">
            {{ film.source.name }}
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { filmLists: [] };
  },
  watch: {
    filmLists() {
      console.log(this.filmLists);
    },
  },
  created() {
    axios
      .get(
        "https://newsapi.org/v2/top-headlines?country=th&apiKey=79c456b534884b9398cbdb580720ea75"
      )
      .then((response) => (this.filmLists = response.data.articles))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
.box {
  width: 190px;
  height: 190px;
  color: black;
}
</style>
