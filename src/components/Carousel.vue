<template>
  <div class="carousel-container">
    <div class="carousel">
      <CarouselItem v-for="item in data" :key="item.code" :item="item" />
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
  },
  props: {
    data: {
      type: Array
    }
  }
}
</script>