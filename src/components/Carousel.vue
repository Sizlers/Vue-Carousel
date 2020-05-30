<template>
  <div class="carousel-container">
    <div class="carousel">
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
        <CarouselItem />
    </div>
    <button class="carousel-button carousel-button--prev"><i class="fas fa-chevron-left"></i></button>
    <button class="carousel-button carousel-button--next"><i class="fas fa-chevron-right"></i></button>
  </div>
</template>

<script>
import CarouselItem from './carousel/CarouselItem.vue'

export default {
  name: 'Carousel',
  components: {
    CarouselItem
  }
}
</script>