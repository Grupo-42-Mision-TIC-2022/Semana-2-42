<template>
  <!-- news -->

<div id="news" class="row mt-md-5 mt-sm-5 mt-xs-5">
  <div class="col-lg-6 col-xs-12" v-for="(pelicula, index) of peliculas" :key="index">
      <div class="d-flex justify-content-center align-items-center">
          <div class="p-3">
              <img v-bind:src='pelicula.Poster' alt="Poster">
          </div>
          <hr>
          <div class="p-2">
              <h2>{{ pelicula.Title }}</h2>
              <p> Año: {{ pelicula.Year }}</p>
              <p> ID de IMDb: {{ pelicula.imdbID }}</p>
              <p> Tipo: {{ pelicula.Type }}</p>
          </div>
          <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
              <a v-bind:href="'https://www.imdb.com/title/' + pelicula.imdbID" target="_blank" class="btn btn-outline-info">Enlace a IMDb</a>
          </div>
      </div>
  </div>
</div>

</template>

<script>
import axios from 'axios'

export default {
  name: 'NewsAPI',
  data () {
    return {
      peliculas: null
    }
  },
  mounted () {
    axios
      .get('http://www.omdbapi.com/?s=star+wars&apikey=6db682b7')
      .then(response => {(this.peliculas = response.data.Search.slice(0, 4))})
  } 
}
</script>

<style scoped>

</style>

