<template>
  <div id="app">
  <carousel>
    <carousel-slide v-for="n in slides" :key="n.id" :index="n - 1">
      <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color: #FFF; font-size:16px;">Hello slide {{ n }}</div>
      <img :src="require('../images/mario-' + n + '.png')" style="width: 100%">
    </carousel-slide>
  </carousel>
  <button @click="addSlide">Ajouter un Slide</button>
  <button @click="removeSlide">Supprimer un Slide</button>
  </div>
</template>

<script>
import Carousel from './components/carousel/Carousel'
import CarouselSlide from './components/carousel/CarouselSlide'

export default {
  name: 'App',
  data () {
    return {
      slides: 2
    }
  },
  components: {
    Carousel,
    CarouselSlide
  },
  methods:{
    addSlide(){
      this.slides++
    },
    removeSlide(){
      this.slides--
    }
  }
}
</script>
