<template>
  <!-- news -->
    <div id="news" class="container-fluid">
        <div class="row mt-md-5 mt-sm-5 mt-xs-5">

            <div class="col-lg-6 col-xs-12">
                <div class="d-flex justify-content-center align-items-center">
    
                    <div class="p-3">
                        <img v-bind:src='pelicula1.poster' alt="">
                    </div>
    
                    <div class="p-2">
                        <h2>{{ pelicula1.titulo }}</h2>
                        <p> Año: {{ pelicula1.anno }}</p>
                        <p> Director: {{ pelicula1.director }}</p>
                        <p> Protagonistas: {{ pelicula1.actores }}</p>
                        <p>{{ pelicula1.trama }}</p>
                    </div>
    
                </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <a v-bind:href="'https://www.imdb.com/title/' + pelicula1.imdbID" class="btn btn-outline-info">Enlace a IMDb</a>
                </div>
            </div>
    
            <div class="col-lg-6 col-xs-12">
                <div class="d-flex justify-content-center align-items-center">
    
                    <div class="p-3">
                        <img v-bind:src='pelicula2.poster' alt="">
                    </div>
    
                    <div class="p-2">
                        <h2>{{ pelicula2.titulo }}</h2>
                        <p> Año: {{ pelicula2.anno }}</p>
                        <p> Director: {{ pelicula2.director }}</p>
                        <p> Protagonistas: {{ pelicula2.actores }}</p>
                        <p>{{ pelicula2.trama }}</p>
                    </div>
    
                </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <a v-bind:href="'https://www.imdb.com/title/' + pelicula2.imdbID" class="btn btn-outline-info">Enlace a IMDb</a>
                </div>
            </div>
    
            <div class="w-100"></div>
    
            <div class="col-lg-6 col-xs-12">
                <div class="d-flex justify-content-center align-items-center">
    
                    <div class="p-3">
                        <img v-bind:src='pelicula3.poster' alt="">
                    </div>
    
                    <div class="p-2">
                        <h2>{{ pelicula3.titulo }}</h2>
                        <p> Año: {{ pelicula3.anno }}</p>
                        <p> Director: {{ pelicula3.director }}</p>
                        <p> Protagonistas: {{ pelicula3.actores }}</p>
                        <p>{{ pelicula3.trama }}</p>
                    </div>
    
                </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <a v-bind:href="'https://www.imdb.com/title/' + pelicula3.imdbID" class="btn btn-outline-info">Enlace a IMDb</a>
                </div>
            </div>

            <div class="col-lg-6 col-xs-12">
                <div class="d-flex justify-content-center align-items-center">
    
                    <div class="p-3">
                        <img v-bind:src='pelicula4.poster' alt="">
                    </div>
    
                    <div class="p-2">
                        <h2>{{ pelicula4.titulo }}</h2>
                        <p> Año: {{ pelicula4.anno }}</p>
                        <p> Director: {{ pelicula4.director }}</p>
                        <p> Protagonistas: {{ pelicula4.actores }}</p>
                        <p>{{ pelicula4.trama }}</p>
                    </div>
    
                </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <a v-bind:href="'https://www.imdb.com/title/' + pelicula4.imdbID" class="btn btn-outline-info">Enlace a IMDb</a>
                </div>
            </div>
    
        </div>
    </div>
</template>

<script>
export default {
  name: 'NewsAPI',
  props: {
    msg: String
  },
  data () {
    return {
      pelicula1: {
        poster: null,
        titulo: null,
        anno: null,
        director: null,
        actores: null,
        trama: null,
        imdbID: null,
      },
      pelicula2: {
        poster: null,
        titulo: null,
        anno: null,
        director: null,
        actores: null,
        trama: null,
        imdbID: null,
      },
      pelicula3: {
        poster: null,
        titulo: null,
        anno: null,
        director: null,
        actores: null,
        trama: null,
        imdbID: null,
      },
      pelicula4: {
        poster: null,
        titulo: null,
        anno: null,
        director: null,
        actores: null,
        trama: null,
        imdbID: null,
      },
    }
  },
  mounted () {
    // Película 1
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.poster = response.data.Poster)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.titulo = response.data.Title)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.anno = response.data.Year)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.director = response.data.Director)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.actores = response.data.Actors)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.trama = response.data.Plot)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0120338&apikey=6db682b7')
      .then(response => (this.pelicula1.imdbID = response.data.imdbID)),
    // Película 2
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.poster = response.data.Poster)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.titulo = response.data.Title)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.anno = response.data.Year)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.director = response.data.Director)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.actores = response.data.Actors)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.trama = response.data.Plot)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0076759&apikey=6db682b7')
      .then(response => (this.pelicula2.imdbID = response.data.imdbID)),
    // Película 3
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.poster = response.data.Poster)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.titulo = response.data.Title)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.anno = response.data.Year)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.director = response.data.Director)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.actores = response.data.Actors)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.trama = response.data.Plot)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0167260&apikey=6db682b7')
      .then(response => (this.pelicula3.imdbID = response.data.imdbID)),
    // Película 4
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.poster = response.data.Poster))
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.titulo = response.data.Title)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.anno = response.data.Year)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.director = response.data.Director)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.actores = response.data.Actors)),
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.trama = response.data.Plot))
    this.$axios
      .get('http://www.omdbapi.com/?i=tt0108052&apikey=6db682b7')
      .then(response => (this.pelicula4.imdbID = response.data.imdbID))
  } 
}
</script>

<style scoped>

</style>

