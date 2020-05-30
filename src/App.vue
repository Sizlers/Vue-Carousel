<template>
  <section class="container">
    <div id="app">
      <h3 class="header-three">Related products</h3>
      <Carousel />
    </div>
  </section>
</template>
<script>
  import Carousel from './components/Carousel.vue'
  // here be import for Myriad font if had licence (chosen as used on distrelec website) 

  export default {
    name: 'App',
    components: {
      Carousel
    }
  }
</script>

<style lang="scss">
    @import "./assets/styles/app.scss";
    @import "./assets/styles/basic/base.scss";
</style>

