<template>
  <section id="profile">
    <a href="https://www.paraplue-illustration.com/">
      <img
        class="profile__image"
        src="../assets/me.png" 
        alt="A girl with pink hair, glasses, and a cat sitting while looking at a laptop"
        title="Artwork by Paraplue Illustrations" 
      />
    </a>

    <div class="profile__info">
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

<script>
  export default {
    data () {
      return {
        publicPath: process.env.BASE_URL,
      }
    }
  }
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #profile {
    display: flex;
    flex-direction: column;
    align-items: center;
    
    margin: 20px auto 0;
    min-height: 600px;

    @include tablet-portrait {
      margin: 0 auto;
      min-height: unset;

      flex-direction: row-reverse;
      justify-content: space-between;
    }

    @include desktop {
      width: 1100px;
    }
  }

  .profile__image {
    height: 300px;
    max-width: 600px;

    @include tablet-portrait {
      height: unset;
      width: 400px;
    }

    @include tablet-landscape {
      width: 500px;
    }
  }

  .profile__info {
    display: flex;
    flex-direction: column;
    justify-content: center;

    @include tablet-portrait {
      padding-right: 20px;
      max-width: 50%;
    }
  }

  .profile__text--h1, .profile__text--h2, .profile__text--h3 {
    margin: 2px 0;
  }

  .profile__text--h1 {
    font-size: 28px;
    font-weight: 600;

    @include tablet-landscape {
      font-size: 48px;
    }
  }

  .profile__text--h1--highlight {
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, $highlight 50%);
    border-radius: 2px;
    padding: 0 3px;
  }

  .profile__text--h2 {
    font-size: 22px;
    font-weight: 500;

    @include tablet-landscape {
      font-size: 36px;
    }
  }

  .profile__text--h3 {
    font-size: 16px;
    font-weight: 400;
    margin: 8px 0 2px;

    @include tablet-landscape {
      font-size: 18px;
      margin: 10px 0 2px;
    }
  }

  .profile__paragraph {
    color: $paragraph;
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    margin: 5px 0;

    @include respond-to-height(700px) {
      margin: 15px 0;
      font-size: 20px;
    }
  }

  .profile__buttons {
    display: flex;
    flex-direction: row;

    @include desktop {
      display: unset;
    }
  }

  .profile__button--filled, .profile__button--outline {
    border-radius: 20px;
    flex: 1 1 0;
    font-weight: 600;
    padding: 12px 15px;
    width: 150px;
    position: relative;
    overflow: hidden;
    transition: all .5s ease-in-out;
  }

  .profile__button--filled {
    background: $objective;
    color: #fefefe;
    margin: 0 10px 0 0;

    &:hover {
      background: darken($objective, 8%);
      color: #fff;
    }
  }

  .profile__button--outline {
    color: $objective;
    border: 2px solid $highlight;
    z-index: 1;

    &:before {
      content: '';
      position: absolute;
      z-index: -1;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      background-color: $highlight;
      transform: translateX(-100%);
      transition: all .5s ease-in-out;
    }

    &:hover {
      color: #fff;
      border-color: transparent;

      &:before {
        background: darken($objective, 8%);
        transform: translateX(0%);
      }
    }
  }
</style>