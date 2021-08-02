<template>
  <section id="profile">
    <img
      class="profile__image"
      src="../assets/me.png" 
      alt="A girl with pink hair, glasses, and a cat sitting while looking at a laptop"
      title="Artwork by Paraplue Illustrations" 
    />

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
          If you'd like to get in touch and learn more about me, or to work on something together,
          please get in touch with me at <a href="mailto:myumiak@gmail.com">myumiak@gmail.com</a>.
        </p>
      </div>

      <div class="profile__buttons">
        <button class="profile__button--filled">Contact Me</button>
        <button class="profile__button--outline">Download CV</button>
      </div>
    </div>
  </section>
</template>

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
      height: unset;
    }

    @include tablet-landscape {
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
      width: 500px;
    }
  }

  .profile__info {
    display: flex;
    flex-direction: column;
    justify-content: center;

    @include tablet-landscape {
      width: 50%;
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
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, $pink 50%);
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

    @include tablet-landscape {
      font-size: 18px;
    }
  }

  .profile__paragraph {
    color: $sub-text;
    font-size: 18px;
    font-weight: 300;
    line-height: 1.3;
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
  }

  .profile__button--filled {
    background: linear-gradient(90deg, $magenta 0%, $peach 100%);
    color: $white;
    margin: 0 10px 0 0;
  }

  .profile__button--outline {
    color: $magenta;
    border: 2px solid $pink;
  }
</style>