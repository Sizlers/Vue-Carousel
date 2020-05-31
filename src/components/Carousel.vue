<template>
  <div class="carousel-container">
    <div class="carousel-track">
      <div class="carousel">
        <CarouselItem v-for="item in data" :key="item.code" :item="item" :classList="carouselItemclassList" />
      </div>
    </div>

    <button v-on:click="handlePrev" class="carousel-button carousel-button--prev"><i class="fas fa-chevron-left"></i></button>
    <button v-on:click="handleNext" class="carousel-button carousel-button--next"><i class="fas fa-chevron-right"></i></button>
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
  },
  methods: {
    handlePrev: function() {
      if (this.canSliderUpdate) {
        this.canSliderUpdate = false;
        this.carouselItemclassList = 'carousel-item__transition-prev'
        setTimeout(() => {
          this.data.push(this.data[0])
          this.data.shift();
          this.carouselItemclassList = ''
          this.canSliderUpdate = true;
        }, 500)
      }
    },
    handleNext: function() {
      if (this.canSliderUpdate) {
        this.canSliderUpdate = false;
        this.data.unshift(this.data[this.data.length - 1])
        this.data.pop();
        this.carouselItemclassList = 'carousel-item__transition-next'
        setTimeout(() => {
          this.carouselItemclassList = ''
          this.canSliderUpdate = true;
        }, 500);
      }
    }
  }, 
  data: function() {
    return {
      carouselItemclassList: '',
      canSliderUpdate: true
    }
  },
  beforeMount() {
    window.setInterval(() => {
      this.handleNext();
    }, 5000);   
  }
}
</script>