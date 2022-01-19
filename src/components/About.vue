<template>
  <section id="about">
    <h1 class="about__h1">
      <span class="about__h1--highlight">About me</span>
    </h1>
    <div class="about__content">
      <img class="about__image" src="https://images.unsplash.com/photo-1534179523731-b2922018150a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80" alt='Photo of Mayumi' />
      <div class="about__info">
        <p>
          Descended from Japanese royalty and a childhood addiction to Neopets, I started with the basics of programming at an early age. 
          An in-game CSS guide gave me my first dip into code. 
          However, it wasn't until high school that I realized HTML, CSS, and JavaScript wasn't just for Neopets.
        </p>

        <p>
          Since then, I have travelled across the country to work as a video game developer, and flown back home to to the east coast pursue software development. 
          Finally, I have come full circle to the niche that fills me with the most joy: web development. As for that, I like where I live now and don't plan on ever moving for work again,
          so for us to be a perfect fit, the role <b>needs to be remote</b>.
        </p>

        <p>
          I have a formal education in Computer Science, but all of my web development knowledge and skills are self-taught, driven entirely by a need to make <i>things</i>. 
          I love working on side projects for fun, but when it comes to professional work, I prefer to stick to non-profit, programs with socioeconomic impact, or something that interests me enough personally.
        </p>
        <p>
          I care about making technology as accessible as possible. I value making things look nice just as much as they function intuitively.
        </p>
        <p>Outside of dev, I love playing games with my friends, riding horses (hunter/jumper, for the fellow horse people out there!), making very specific playlists on Spotify, building custom mechanical keyboards, and cooking.</p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use "../sass/breakpoints";
  @use "../sass/colors";
  @use "../sass/fonts";
  @use "../sass/spacing";

  #about {
    @include spacing.section-spacing;
  }

  .about__h1 {
    font-size: fonts.$font-size-8;

    @include breakpoints.tablet-landscape {
      font-size: fonts.$font-size-9;
    }

    @include spacing.element-spacing;
  }

  .about__h1--highlight {
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, colors.$highlight 50%);
    border-radius: 2px;
    padding: 0 3px;
  }

  .about__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    @include breakpoints.tablet-landscape {
      flex-direction: row-reverse;
      align-items: unset;
    }
  }

  .about__image {
    border-radius: 10px;
    max-width: 100%;

    @include breakpoints.tablet-portrait {
      width: 350px;
    }

    @include breakpoints.tablet-landscape {
      width: 550px;
    }

    @include spacing.image-spacing-reverse;
  }

  .about__info {
    p {
      @include spacing.paragraph-spacing;
    }
    @include breakpoints.tablet-landscape {
      flex: 1 1 0;
    }
  }
</style>