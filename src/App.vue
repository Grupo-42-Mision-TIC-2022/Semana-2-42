<template>
    <div id="app">
        <HeaderTop></HeaderTop>
        <CarouselHeader></CarouselHeader>
        <Services></Services>
        <div class="container-fluid">
                  <NewsAPI></NewsAPI>
        </div>
        <div class="container-fluid">
            <div class="row justify-content-center mb-5">
                <div class="col mt-4" v-for="(item, index) of member" :key="index" >
                    <TeamCard v-bind:member="item"></TeamCard>
                </div>
            </div>
        </div>
        <PageFooter></PageFooter>
    </div>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue'
import CarouselHeader from './components/CarouselHeader.vue'
import Services from './components/Services.vue'
import NewsAPI from './components/NewsAPI.vue'
import TeamCard from './components/TeamCard.vue'
import PageFooter from "./components/PageFooter"

export default {
  name: 'App',
  components: {
  HeaderTop,
  CarouselHeader,
  Services,
  NewsAPI,
  TeamCard,
  PageFooter
  },
  data() {
    return {
      title: "Conoce más de nosotros!",
        member:[
          {
          codigo:1,
          nombre:"Juan Carlos Moreno",
          descripcion:"Ingeniero electrónico de la Universidad Nacional de Colombia, tiene 39 años y dentro de sus pasatiempos están: Leer y  jugar juegos de mesa",
          rol:"Desarrollador backend",
          image:"https://i.postimg.cc/Z5khmVW2/Juan-Morenoblack.jpg",
          },
          {
          codigo:2,
          nombre:"Juan Carlos Yepes",
          descripcion:"Médico de la Universidad de Antioquia, tiene 42 años, dentro de sus pasatiempos favoritos esta disfrutar del Cine y las nuevas tecnologías",
          rol:"Arquitecto de Software",
          image:"https://i.postimg.cc/MTJcjy3F/Juan-Yepesblack.jpg",
          },
          {
          codigo:3,
          nombre:"Omar J. Rodriguez",
          descripcion:"Ingeniero Químico de la Universidad Nacional de Colombia, tiene 45 años, dentro de sus pasatiempos favoritos están: el cine y ciclismo",
          rol:"Tester",
          image:"https://i.postimg.cc/brXKPvJb/Omarblack.jpg",
          },
          {
          codigo:4,
          nombre:"Diana Rocio Moreno",
          descripcion:"Diseñadora Industrial de la Universidad Pedagógica y Tecnológica de Colombia, tiene 25 años, dentro de sus pasatiempos favoritos están: Leer y hacer ejercicio",
          rol:"Analista",
          image:"https://i.postimg.cc/nhwSZLSz/Diana-Moreno.jpg",
          }
          ],
      }
  }
}
</script>
