<template>
  <section id="profile">
    <a href="https://www.paraplue-illustration.com/">
      <img
        class="profile__image"
        src="../assets/me.png" 
        alt="A girl with pink hair, glasses, and a cat sitting while looking at a laptop"
        title="Artwork by Paraplü Illustrations" 
      />
    </a>

    <div class="profile__info">
      <!-- <Navigation /> -->

      <div class="profile__text">
        <h1 class="profile__text--h1"> 
          Hi, I’m
          <span class="profile__text--h1--highlight">Mayumi</span>.
        </h1>
        <h2 class="profile__text--h2">I’m a web developer and designer based anywhere.</h2>
        <h3 class="profile__text--h3">(That means I like to work remotely.)</h3>
        <p class="profile__paragraph">
          I'm currently redesigning this site and updating it with my most recent projects.
          If you'd like to work on something together,
          please get in touch with me <a href="mailto:me@mayumi.dev">via email</a>.
        </p>
      </div>

      <div class="profile__buttons">
        <a href="mailto:me@mayumi.dev"><button class="profile__button--filled">Contact Me</button></a>
        <a href="Complete CV.pdf" download="Mayumi Ohara CV"><button class="profile__button--outline">Download CV</button></a>
      </div>
    </div>
  </section>
</template>

<!-- <script>
import Navigation from './Navigation';

export default {
  name: 'Profile',
  components: { 
    Navigation, 
  }
}
</script> -->

<style lang="scss">
  @use "../sass/breakpoints";
  @use "../sass/colors";
  @use "../sass/fonts";
  @use "../sass/spacing";

  #profile {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;

    @include breakpoints.tablet-portrait {
      flex-direction: row-reverse;
      justify-content: space-between;
    }

    @include spacing.section-spacing;
  }

  .profile__image {
    height: 320px;
    margin: 0 0 (spacing.$row-gutter * 3);

    @include breakpoints.tablet-portrait {
      height: 390px;
      margin: 0;
    }

    @include breakpoints.tablet-landscape {
      height: 500px;
    }

    @include breakpoints.desktop {
      height: 565px;
    }
  }

  .profile__info {
    display: flex;
    flex-direction: column;

    @include breakpoints.tablet-portrait {
      flex: 1 1 0;
      margin: 0 spacing.$column-gutter 0 0;
    }
  }

  .profile__text--h1 {
    font-size: fonts.$font-size-8;
    font-weight: 600;

    @include breakpoints.tablet-landscape {
      font-size: fonts.$font-size-9;
    }

    .profile__text--h1--highlight {
      background: linear-gradient(180deg, rgba(255,255,255,0) 50%, colors.$highlight 50%);
      border-radius: 2px;
      padding: 0 3px;
    }

    @include spacing.large-header-spacing;
  }

  .profile__text--h2 {
    font-size: fonts.$font-size-6;
    font-weight: 500;

    @include breakpoints.tablet-landscape {
      font-size: fonts.$font-size-8;
      max-width: 520px;
    }

    @include spacing.header-spacing;
  }

  .profile__text--h3 {
    font-size: fonts.$font-size-3;
    font-weight: 400;

    @include breakpoints.tablet-landscape {
      font-size: fonts.$font-size-3;
    }

    @include spacing.element-spacing;
  }

  .profile__paragraph {
    @include breakpoints.tablet-landscape {
      max-width: 450px;
    }

    @include spacing.element-spacing;
  }

  .profile__buttons {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    @include breakpoints.tablet-portrait {
      justify-content: unset;
    }
  }

  .profile__button--filled {
    background: colors.$objective;
    color: #FEFEFE;

    &:hover {
      background: darken(colors.$objective, 8%);
      color: #FFFFFF;
    }

    @include breakpoints.tablet-portrait {
      margin: 0 15px 0 0;
    }

    @include breakpoints.tablet-landscape {
      min-width: 180px;
    }
  }

  .profile__button--outline {
    color: colors.$objective;
    border: 2px solid colors.$highlight;
    z-index: 1;

    &:before {
      content: '';
      position: absolute;
      z-index: -1;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      background-color: colors.$highlight;
      transform: translateX(-100%);
      transition: all .6s ease-in-out;
    }

    &:hover {
      color: #FFFFFF;
      border-color: transparent;

      &:before {
        background: darken(colors.$objective, 8%);
        transform: translateX(0%);
      }
    }

    @include breakpoints.tablet-landscape {
      min-width: 180px;
    }
  }
</style>