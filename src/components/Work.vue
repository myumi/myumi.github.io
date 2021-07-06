<template>
  <div id="work">
    <div class="work__headers">
      <h1 class="headers__h1 headers__h1--highlight">Work</h1>
      <h2 class="headers__h2">These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--projects">
      <WorkItem
        v-for="(project, index) in projects"
        :key="project.title"
        :class="index % 2 ? '' : 'flipped'"
        :image="project.image"
        :imageAlt="project.imageAlt"
        :label="project.label"
        :title="project.title"
        :tools="project.tools"
        :description="project.description"
        :recognitions="projects.recognitions"
        :github="projects.github"
      />
    </div>
  </div>
</template>

<script>
import WorkItem from './WorkItem.vue'

export default {
  components: {
    WorkItem 
  },
  data() {
    return {
      projects: [
        {
          image: 'Vibrant',
          imageAlt: `A collection of designs and mockups`,
          label: 'Web apps and design',
          title: 'Vibrant Emotional Health',
          tools: ['React', 'Gatsby', 'Vue', 'SCSS', 'Figma'],
          description: `I worked alongside two other developers to develop and design an 
            application that supports a community with tens of millions of users. This project was built in Vue, integrating and updating a similar tool
            one of the other developers had worked on, as well as a version of the ZXing library by Google I modified to support our needs.
            As well as development, my responsibilites included moderating the Discord community for the project as well as answering user questions and
            applying changes and fixes to suite the ever-changing needs of the community.`,
          recognitions: {
            featured: ['Wall Street Journal', 'Kotaku', 'Polygon', 'Washington Post'],
            forked: ['Getty Museum', 'the Metropolitan Museum of Art', 'Jackbox Games'],
            used: ['the Joe Biden Campaign', 'and more']
          },
        },
        {
          image: 'acpatterns',
          imageAlt: `A snapshot of a website that emulates the pattern-making tool 
            in the Nintendo Switch game Animal Crossing: New Horizions`,
          label: 'Web App',
          title: 'ACPatterns',
          tools: ['Vue', 'SCSS'],
          description: `I worked alongside two other developers to develop and design an 
            application that supports a community with tens of millions of users. This project was built in Vue, integrating and updating a similar tool
            one of the other developers had worked on, as well as a version of the ZXing library by Google I modified to support our needs.
            As well as development, my responsibilites included moderating the Discord community for the project as well as answering user questions and
            applying changes and fixes to suite the ever-changing needs of the community.`,
          recognitions: {
            featured: ['Wall Street Journal', 'Kotaku', 'Polygon', 'Washington Post'],
            forked: ['Getty Museum', 'the Metropolitan Museum of Art', 'Jackbox Games'],
            used: ['the Joe Biden Campaign', 'and more']
          },
        },
        {
          image: 'acpatterns',
          imageAlt: `A snapshot of a website that emulates the pattern-making tool 
            in the Nintendo Switch game Animal Crossing: New Horizions`,
          label: 'Web App',
          title: 'ACPatterns',
          description: `I worked alongside two other developers to develop and design an 
            application that supports a community with tens of millions of users. This project was built in Vue, integrating and updating a similar tool
            one of the other developers had worked on, as well as a version of the ZXing library by Google I modified to support our needs.
            As well as development, my responsibilites included moderating the Discord community for the project as well as answering user questions and
            applying changes and fixes to suite the ever-changing needs of the community.`,
          recognitions: {
            featured: ['Wall Street Journal', 'Kotaku', 'Polygon', 'Washington Post'],
            forked: ['Getty Museum', 'the Metropolitan Museum of Art', 'Jackbox Games'],
            used: ['the Joe Biden Campaign', 'and more']
          },
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #work {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 20px auto 0;
    min-height: 600px;

    @include tablet-portrait {
      width: 500px;
    }

    @include tablet-landscape {
      width: 1100px;
    }
  }

  .work__headers {
    width: 100%;
  }

  .headers__h1 {
    display: inline;
    font-size: 28px;
    font-weight: 600;

    @include tablet-landscape {
      font-size: 48px;
    }
  }

  .headers__h1--highlight {
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, $pink 50%);
    border-radius: 2px;
    padding: 0 3px;
  }

  .headers__h2 {
    font-size: 22px;
    font-weight: 500;

    @include tablet-landscape {
      font-size: 24px;
    }
  }
</style>