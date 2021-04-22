<template>
  <div id="carousel" :class="{clockwise: moveClockwise }">
    <CarouselItem 
      v-for="(item, index) in projects" 
      :key="index" 
      :class="{ active: index === current, left: index === left, right: index === right }"
      :title="item.title" 
      :description="item.description" 
      :image="item.image"
    />
    <!-- carousel move arrows -->
    <div class="carousel--dot-container">
      <div
        class="carousel--dot"
        v-for="(item, index) in projects" 
        :key="index"
        :class="{ active: index === current }"
      >
      </div>
    </div>
  </div>
</template>

// https://www.w3schools.com/howto/howto_js_slideshow.asp
// will make styling easier

// slideshow that shows 3 items
// item 0 is left, item 1 is "active", item 2 is right and any past that are hidden
// show the item that is active and then items next to it?
// if item == last, show item=0 to right
// if item == 0, show item=last to left

// maybe just start with simple arrows, lefts & right
// show 3 at a time
// one on top is "left", center is "active", bottom is "right"

<script>
import CarouselItem from './CarouselItem'

export default {
  name: 'Carousel',
  components: { CarouselItem },
  data() {
    return {
      left: 0,
      current: 1,
      right: 2,
      moveClockwise: true,
      projects: [
        {
          name: 'acpatterns.com',
          description: `I worked alongside two other developers to develop and design an application that supports the Animal Crossing: New Horizions and Animal Crossing: New Leaf communities, each with tens of millions of unique users. The application was built with Vue and integrated unique QR Code reading and writing libraries.`,
          list: ['Featured in Wall Street Journal, Kotaku, Polygon, Washington Post', 'Forked by Getty Museum, the Metropolitan Museum of Art, Jackbox Games', 'Used by the Joe Biden 2020 Campaign and more'],
          image: {
            path: '../assets/acpatterns.png',
            alt: 'A screenshot of the acpatterns.com pattern-drawing tool'
          },
        },
        {
          name: 'vibrant: emotional health',
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quis eleifend lacus. 
          Nunc tincidunt volutpat tempor. Integer imperdiet eros quis velit aliquet, in consectetur lorem vulputate. Aenean vitae tempus leo. Donec lorem tortor, fermentum 
          a venenatis at, tincidunt at orci. Cras ultricies erat porta euismod lobortis. Praesent pulvinar congue elementum.
          Aliquam convallis nibh consequat lectus efficitur convallis. Etiam laoreet lorem lectus, eget pharetra erat consequat quis. Etiam tincidunt ultrices vehicula.`,
          image: {
            path: '',
            alt: 'Two mobile devices showing different designs on their screens'
          },
        },
        {
          name: 'novamei',
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quis eleifend lacus. 
          Nunc tincidunt volutpat tempor. Integer imperdiet eros quis velit aliquet, in consectetur lorem vulputate. Aenean vitae tempus leo. Donec lorem tortor, fermentum 
          a venenatis at, tincidunt at orci. Cras ultricies erat porta euismod lobortis. Praesent pulvinar congue elementum.
          Aliquam convallis nibh consequat lectus efficitur convallis. Etiam laoreet lorem lectus, eget pharetra erat consequat quis. Etiam tincidunt ultrices vehicula.`,
          image: {
            path: '',
            alt: 'Novamei logo'
          },
        },
        {
          name: 'discord bots',
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quis eleifend lacus. 
          Nunc tincidunt volutpat tempor. Integer imperdiet eros quis velit aliquet, in consectetur lorem vulputate. Aenean vitae tempus leo. Donec lorem tortor, fermentum 
          a venenatis at, tincidunt at orci. Cras ultricies erat porta euismod lobortis. Praesent pulvinar congue elementum.
          Aliquam convallis nibh consequat lectus efficitur convallis. Etiam laoreet lorem lectus, eget pharetra erat consequat quis. Etiam tincidunt ultrices vehicula.`,
          image: {
            path: '',
            alt: 'Discord logo'
          }
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
#carousel {
  .carousel--dot-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 0 auto;
    height: 15px;
    width: 100px;

    .carousel--dot {
      height: 15px;
      width: 15px;

      border-radius: 100%;
      background-color: lightgrey;

      &.active {
        background-color: darkgrey;
      }
    }
  }
}
</style>
