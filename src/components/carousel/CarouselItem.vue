<template>
  <div class="carousel-item carousel-item__transition-auto" :class="classList">
    <a class="carousel-item__container" :href="item.url">
      <div class="carousel-item__image-container">
        <img class="carousel-item__image" :title="item.name" :alt="item.productImageAltText" :src="item.productImageUrl">
      </div>
      <div>
        <div class="carousel-item__header-container">
          <h3 class="carousel-item__title">{{item.name}}</h3>
        </div>
        <!-- I hardcoded the below as stock levels didn't appear to be in the JSON -->
        <p class="carousel-item__stock">Stock: <span>10</span></p>
        <p class="carousel-item__price">{{item.price.currency}} <span>{{item.price.formattedValue}}</span></p>
        <button class="button button--blue">Buy now</button>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: 'CarouselItem', 
  props: {
    item: {
      type: Object
    },
    classList: {
      type: String
    },
  }
}
</script>