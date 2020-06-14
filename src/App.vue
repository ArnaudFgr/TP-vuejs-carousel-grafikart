<template>
  <div id="app">
  <carousel>
    <carousel-slide>
      <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color: #FFF; font-size:16px;">Hello</div>
      <img src="../images/mario-1.png" style="width: 100%">
    </carousel-slide>
    <carousel-slide>
      <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color: #FFF; font-size:16px;">ByeBye</div>
      <img src="../images/mario-2.png" style="width: 100%">
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
