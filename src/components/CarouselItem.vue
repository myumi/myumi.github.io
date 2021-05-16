<template>
  <div id="carousel-item">
    <img class="carousel-item--image" :src="image.path" :alt="image.alt" />
    <h1 class="carousel-item--title">{{ title }}</h1>
    <p class="carousel-item--description" :html="description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: 'CarouselItem',
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    image: {
      type: Object,
      default: undefined
    }
  },
}
</script>

<style lang="scss" scoped>
#carousel-item {

  .carousel-item--image {

  }

  .carousel-item--title {

  }

  .carousel-item--description {

  }
}
</style>
