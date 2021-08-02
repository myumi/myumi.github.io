<template>
  <section id="about">
    <h1 class="about__h1 about__h1--highlight">About me</h1>
    <div class="about__content">
      <img class="about__image" src="" alt='Photo of Mayumi' />
      <div class="about__info">
        <p>
          Descended from Japanese royalty and a childhood addiction to Neopets, I started with the basics of programming at an early age. 
          An in-game CSS guide gave me my first dip into code. 
          However, it wasn't until high school that I realized HTML, CSS, and JavaScript wasn't just for Neopets.
        </p>

        <p>
          Since then, I have travelled across the country to work as a video game developer, and flown back home to to the east coast pursue software development. 
          Finally, I have come full circle to the niche that fills me with the most joy: web development.
        </p>

        <p>
          I have a formal education in Computer Science, but all of my web development knowledge and skills are self-taught. 
          I love working on side projects for fun, but when it comes to professional work, I prefer to stick to non-profit or programs with socioeconomic impact.
        </p>
        <p>
          I care about making technology as accessible as possible. I value making things look nice just as much as they function intuitively.
        </p>
        <p>Outside of dev, I love playing video games with my friends, riding horses, making very specific playlists on Spotify, and cooking.</p>
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style lang="scss" scoped>
@import '../sass/main.scss';

  #about {
    flex-direction: column;
    margin: 40px auto;

    @include desktop {
      width: 1100px;
    }
  }

  .about__h1 {
    display: inline-block;
    font-size: 28px;
    font-weight: 600;
    margin: 0 0 10px;

    @include tablet-landscape {
      font-size: 48px;
    }
  }

  .about__h1--highlight {
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, $pink 50%);
    border-radius: 2px;
    padding: 0 3px;
  }

  .about__content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    @include tablet-landscape {
      flex-direction: row-reverse;
    }
  }

  .about__image {

    @include tablet-landscape {
      height: 600px;
      width: 500px;
    }
  }

  .about__info {
    align-self: stretch;
    line-height: 1.5;

    @include tablet-landscape {
      width: 500px;
    }
  }

</style>