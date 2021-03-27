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

    @include desktop {
      flex-direction: row;
      justify-content: space-between;
      padding: 0 100px;
      margin: 50px 0;
    }

    .about--image {
      background: #C4C4C4;
      border-radius: 15px;
      min-width: 478px;
      height: 673px;
    }

    .about--info {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      font-size: 18px;
      line-height: 1.8;
      max-width: 420px;
    }
  }
</style>