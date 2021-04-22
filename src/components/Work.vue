<template>
  <div id="work">
    <div class="work--headers">
      <h1>Work</h1>
      <h2>These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--projects">
      <!-- <Project 
        v-for="{ name, description, list, image } in projects"
        :name="name"
        :description="description"
        :list="list"
        :image="image"
        :key="name"
      /> -->
      <Carousel />
    </div>
  </div>
</template>

<script>
import Carousel from './Carousel'

export default {
  components: { Carousel }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #work {
    color: $dark-grey;
    padding: 10px 40px;
    margin: auto;
    max-width: 1200px;

    @include tablet-portrait {
      padding: 30px 50px;
    }

    .work--headers {
      text-align: left;

      h1 {
        display: block;
        font-size: 48px;
        font-weight: 600;
        line-height: 58px;
      }

      h2 {
        font-weight: 400;
      }
    }
    
    .work--projects {
      // display: none;
    }
  }
</style>