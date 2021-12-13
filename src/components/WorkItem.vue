<template>
  <section class="work-item">
    <img class="work-item__image" :src="image" :alt="imageAlt" :title="`Artwork in progress! Placeholder image by Sharon McCutcheon on UnSplash.`"/>
    <div class="work-item__text-content">
      <span class="work-item__label">{{ label }}</span>
      <h1 class="work-item__title">{{ title }}</h1>
      <span class="work-item__tools">{{ tools.join(', ') }}</span>
      <div class="work-item__description" v-html="description"></div>
      <ul v-if="recognitions" class="work-item__awards">
        <li v-for="award in recognitions" :key="award.type">
          <i>{{ award.type }}</i> by {{ award.names.join(', ') }}
        </li>
      </ul>
      <a 
        v-if="github"
        :href="github"
        class="work-item__github"
      >
      <IconGitHub />
      View this project on GitHub
      </a>
    </div>
  </section>
</template>

<script>
import IconGitHub from './icons/IconGitHub.vue';
export default {
  name: 'WorkItem',
  props: {
    image: {
      type: String,
      default: ''
    },
    imageAlt: {
      type: String,
      default: ''
    },
    label: {
      type: String,
      default: 'Project'
    },
    title: {
      type: String,
      default: 'Project'
    },
    tools: {
      type: Array,
      default: () => []
    },
    description: {
      type: String,
      default: ''
    },
    recognitions: {
      type: Array,
      default: () => [],
    },
    github: {
      type: String,
      default: ''
    },
  },
  components: {
    IconGitHub,
  }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  .work-item {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 40px auto 10px;

    width: 100%;

    @include tablet-landscape {
      flex-direction: row;
      justify-content: space-between;

      margin: 50px auto;
      min-height: 600px;
    }

    &:last-of-type {
      margin: 0;
    }
  }

  .work-item__image {
    align-self: stretch;
    width: 100%;
    margin: 0 auto 20px;
    border-radius: 10px;

    @include tablet-portrait {
      width: 550px;
    }
    
    @include tablet-landscape {
      margin: unset;
    }
  }

  .work-item__text-content { 
    position: relative;   
    margin: 0 0 40px 0;

    &:last-of-type {
      margin: 0;
    }

    @include tablet-landscape {
      align-self: stretch;
      margin: 0 0 0 50px;
      min-height: unset;
      width: 50%;

      &:last-of-type {
        margin: 0 0 0 50px;
      }
    }
  }

  .work-item__label {
    color: #FF7DAD;
    font-weight: bold;
    font-size: 18px;
    text-transform: uppercase;
  }

  .work-item__title {
    color: #183764;
    font-weight: 500;
    font-size: 36px;
    margin: 10px 0;
  }

  .work-item__tools {
    color: $subheader;
    display: block;
    font-size: 18px;
    font-weight: 500;
    margin: 0 0 15px 0;

    @include tablet-portrait {
      margin: 0 0 30px 0;
    }
  }
  
  .work-item__description {
    p {
      margin: 5px 0;
      line-height: 1.6 !important;

      @include tablet-portrait {
        margin: 8px 0;
      }
    }
  }

  .work-item__awards {
    margin: 0 0 10px;
    line-height: 1.6 !important;

    @include tablet-portrait {
      margin: 10px 0;
    }

    li {
      margin: 5px 0;
    }
  }

  .work-item__github {
    display: inline-flex;
    align-items: center;
    justify-content: space-between;

    color: #FF7DAD;
    font-size: 18px;
    width: 260px;

    &:hover {
      color: #FF7DAD;
    }

    @include tablet-portrait {
      position: absolute;
      bottom: 0;
      left: 0;
    }
  }
</style>
