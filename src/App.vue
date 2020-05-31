<template>
  <section class="container">
    <div id="app">
      <h3 class="header-three">Related products</h3>
      <Carousel :data="carouselData.carouselData" />
    </div>
  </section>
</template>

<script>
  import Carousel from './components/Carousel.vue';
  import carouselData from './data.json';

  export default {
    name: 'App',
    components: {
      Carousel
    },
    data() {
      return {
          carouselData
      }
    }
  }
</script>

<style lang="scss">
    @import "./assets/styles/app.scss";
    @import "./assets/styles/basic/base.scss";
</style>

