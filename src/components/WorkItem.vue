<template>
  <section class="work-item">
    <img class="work-item__image" :src="image" :alt="imageAlt" :title="`Artwork in progress! Placeholder image by Sharon McCutcheon on UnSplash.`"/>
    <div class="work-item__text-content">

      <h2 class="work-item__label">{{ label }}</h2>
      <h1 class="work-item__title">{{ title }}</h1>
      <h3 class="work-item__tools">{{ tools.join(', ') }}</h3>
      <div class="work-item__links">
        <a 
          v-if="url"
          :href="url"
          target="_blank"
          class="work-item__icon"
        >
          <IconWeb />
        </a>

        <a 
          v-if="github"
          :href="github"
          target="_blank"
          class="work-item__icon"
        >
          <IconGitHub />
        </a>
      </div>

      <div class="work-item__description" v-html="description"></div>
      <ul v-if="recognitions.length" class="work-item__awards">
        <li v-for="award in recognitions" :key="award.type">
          <i>{{ award.type }}</i> by {{ award.names.join(', ') }}.
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import IconGitHub from './icons/IconGitHub';
import IconWeb  from './icons/IconWeb';

export default {
  name: 'WorkItem',
  props: {
    image: {
      type: String,
      default: '',
    },
    imageAlt: {
      type: String,
      default: '',
    },
    label: {
      type: String,
      default: 'Project',
    },
    title: {
      type: String,
      default: 'Project',
    },
    tools: {
      type: Array,
      default: () => [],
    },
    description: {
      type: String,
      default: '',
    },
    recognitions: {
      type: Array,
      default: () => [],
    },
    url: {
      type: String,
      default: '',
    },
    github: {
      type: String,
      default: '',
    },
  },
  components: {
    IconGitHub,
    IconWeb,
  }
}
</script>

<style lang="scss">
  @use "../sass/breakpoints";
  @use "../sass/colors";
  @use "../sass/fonts";
  @use "../sass/spacing";

  .work-item {
    display: flex;
    flex-direction: column;
    align-items: center;

    @include breakpoints.tablet-landscape {
      flex-direction: row;
      align-items: unset;
    }

    &:not(:last-child) {
      @include spacing.element-spacing;
    }
  }

  .work-item__image {
    border-radius: 10px;
    max-width: 100%;

    @include breakpoints.tablet-portrait {
      width: 350px;
    }

    @include breakpoints.tablet-landscape {
      width: 550px;
    }

    @include spacing.image-spacing;
  }

  .work-item__text-content {
    @include breakpoints.tablet-landscape {
      flex: 1 1 0;
    }
  }

  .work-item__label {
    color: colors.$objective;
    font-size: fonts.$font-size-4;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;

    @include spacing.large-header-spacing;
  }

  .work-item__title {
    color: colors.$large-header;
    font-weight: 500;
    font-size: fonts.$font-size-7;

    @include breakpoints.tablet-landscape {
      font-size: fonts.$font-size-8;
      padding: -5px 0;
    }

    @include spacing.large-header-spacing;
  }

  .work-item__tools {
    color: colors.$subheader;
    font-size: fonts.$font-size-4;
    font-weight: 500;

    @include spacing.header-spacing;
  }

  .work-item__links {
    a {
      margin: 0 10px 0 0;
    }

    @include spacing.element-spacing;
  }
  
  .work-item__description {
    p {
      @include spacing.paragraph-spacing;
    }
    @include spacing.element-spacing;
  }

  .work-item__awards {
    font-size: fonts.$font-size-3;

    li {
      @include spacing.header-spacing;
    }
  }
</style>
