<template>
  <div class="carousel">
      <CarouselItem />
      <CarouselItem />
      <CarouselItem />
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