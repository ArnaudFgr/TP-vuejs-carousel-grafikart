<template>
  <div class="carousel">
    <slot></slot>
    <button class="carousel__nav carousel__prev" @click.prevent="prev"></button>
    <button class="carousel__nav carousel__next" @click.prevent="next"></button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      index: 0,
      slides: [],
      direction: null
    }
  },

  mounted (){
    this.slides = this.$children
    this.slides.forEach((slide, i) => {
      slide.index = i
    })
  },

  computed: {
    slidesCount () { return this.slides.length }
  },

  methods: {
    next(){
      this.index++
      this.direction = 'right'
      if(this.index >= this.slidesCount){
        this.index = 0
      }
    },
    prev(){
      this.index--
      this.direction = 'left'
      if(this.index < 0){
        this.index = this.slidesCount - 1
      }
    },

  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    border: none;
  }
  .carousel{
    position: relative;
  }
  .carousel__nav{
    position: absolute;
    top: 50%;
    margin-top: -31px;
    left: 10px;
    background: url(prev.png);
    width: 60px;
    height: 60px
  }

  .carousel__nav.carousel__next{
    right: 10px;
    left: auto;
    background-image: url(next.png);
  }

</style>