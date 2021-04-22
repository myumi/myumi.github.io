<template>
  <div id="about">
    <img class="about--image" alt='Photo of Mayumi' />
    <div class="about--info">
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
    </div>
  </div>
</template>

<script>
</script>

<style lang="scss" scoped>
@import '../sass/main.scss';

#about {
  display: flex;
  flex-direction: column;

  color: $dark-grey;
  padding: 40px;
  margin: auto;
  max-width: 1200px;

  @include tablet-portrait {
    justify-content: space-between;
    align-items: center;

    padding: 30px 50px;
  }

  @include desktop {
    flex-direction: row;
    align-content: center;
  }

  .about--image {
    background: #C4C4C4;
    border-radius: 15px;
    text-align: center;
    margin: 0 auto;
    height: 400px;
    width: 350px;

    @include desktop {
      margin: 0;
      height: 673px;
      width: 600px;
    }
  }

  .about--info {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    font-size: 18px;
    line-height: 1.8;
    margin: 10px 0 0;
    max-width: unset;

    p {
      margin: 15px 0 0;
    }

    @include tablet-portrait {
      margin: 30px 0 0;
    }

    @include desktop {
      margin: 0;
      max-width: 420px;
    }
  }
}
</style>