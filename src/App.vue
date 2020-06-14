<template>
  <div id="app">
  <carousel>
    <carousel-slide>
      Salut les gens
    </carousel-slide>
    <carousel-slide>
      Aurevoir les gens
    </carousel-slide>
  </carousel>
  </div>
</template>

<script>
import Carousel from './components/carousel/Carousel'
import CarouselSlide from './components/carousel/CarouselSlide'

export default {
  name: 'App',
  components: {
    Carousel,
    CarouselSlide
  }
}
</script>
