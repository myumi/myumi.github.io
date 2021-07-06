<template>
  <div class="work-item">
    <img class="work-item__image" :src="image" :alt=imageTitle />

    <div class="work-item__text-content">
      <span class="work-item__label">{{ label }}</span>
      <h1 class="work-item__title">{{ title }}</h1>
      <span class="work-item__tools">{{ tools.join(', ') }}</span>
      <div class="work-item__description">{{ description }}</div>
      <a 
        v-if="github"
        :href="github"
        class="work-item__github"
      >
      <!-- githubicon -->
      View this project on GitHub
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "WorkItem",
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
      type: String,
      default: ''
    },
    github: {
      type: String,
      default: ''
    },
  }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  .work-item {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 20px auto 10px;
    min-height: 500px;

    @include tablet-portrait {
      width: 500px;
    }

    @include tablet-landscape {
      flex-direction: row;
      justify-content: space-between;

      margin: 50px auto 25px;
      width: 1100px;
    }

    &.flipped {
      @include tablet-landscape {
        flex-direction: row-reverse;
      }
      .work-item__text-content {
        margin: 0 50px 0 0;
      }
    }
  }

  .work-item__image {
    align-self: stretch;
    width: 550px;
  }

  .work-item__text-content {
    align-self: stretch;

    margin: 0 0 0 50px;
    width: 500px;
  }

  .work-item__label {
    text-transform: uppercase;
  }

  .work-item__title {
    font-weight: 500;
  }

  .work-item__tools {
    color: $link;
    display: block;
    font-size: 14px;
    margin: 0 0 10px 0;
  }
  
  .work-item__description {
    line-height: 1.5;
  }
</style>
