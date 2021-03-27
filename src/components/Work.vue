<template>
  <div id="work">
    <div class="work--headers">
      <h1>Work</h1>
      <h2>These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--circle"></div>
    <div class="work--projects">
      <Project 
        v-for="{ name, description, list, image } in projects"
        :name="name"
        :description="description"
        :list="list"
        :image="image"
        :key="name"
      />
    </div>
  </div>
</template>

<script>
import Project from './Project'

export default {
  components: { Project },
  data() {
    return {
      projects: [
        {
          name: 'acpatterns.com',
          description: `I worked alongside two other developers to develop and design an application that supports the Animal Crossing: New Horizions and Animal Crossing: New Leaf communities, each with tens of millions of unique users. The application was built with Vue and integrated unique QR Code reading and writing libraries.`,
          list: ['Featured in Wall Street Journal, Kotaku, Polygon, Washington Post', 'Forked by Getty Museum, the Metropolitan Museum of Art, Jackbox Games', 'Used by the Joe Biden 2020 Campaign and more'],
          image: {
            src: '../assets/acpatterns.png',
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
            src: '',
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
            src: '',
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
            src: '',
            alt: 'Discord logo'
          }
        },
      ]
    }
  }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  .work--headers {
    text-align: left;
    padding: 0 0 0 50px;

    @include desktop {
      flex-direction: row;
      padding: 0 0 0 100px;
    }

    h1 {
      display: block;
      font-size: 48px;
      font-weight: 600;
      line-height: 58px;
      margin: 80p
      x 0 10px;
    }
    h2 {
      font-weight: 400;
    }
  }
</style>