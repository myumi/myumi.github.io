<template>
  <div id="#profile">
    <div class="profile--header">
      <h1>Hi. I'm <b><i>Mayumi.</i></b></h1>
      <h2>I'm a web developer and designer based anywhere.</h2>
      <h3>(That means I like to work remotely.)</h3>
    </div>
    <div class="profile--bottom-half">
      <Social class="profile--social" />
      <div class="profile--text">
        <div class="text--paragraphs">
          <p>
            Descended from Japanese royalty and a childhood addiction to Neopets, 
            I started with the basics of programming at an early age. An in-game 
            CSS guide gave me my first dip into code, however, it wasn't until high 
            school that I realized HTML/CSS/JS wasn't just for Neopets.
          </p>
          <p>
            Since then, I have travelled across the country to work as a video game 
            developer, and flown back home to to the east coast pursue software 
            development. Finally, I have come full circle to the niche that fills me 
            with the most joy: web development.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Social from './Social.vue'

export default {
  components: { Social }
}
</script>

<style lang="scss" scoped>
@import '../assets/main.scss';
.profile--header {
  margin: 50px 0 0 120px;
}
.profile--bottom-half {
  display: flex;
  flex-direction: row;

  margin: 10vh 0 0;

  .profile--social {
    display: flex;
    flex-direction: column;
    justify-content: center;

    margin: 0 60px;
  }
  .profile--text {
    background-color: $white;
    border-radius: 8px;
    font-size: 18px;
    line-height: 34px;
    padding: 20px 50px;
    width: 100%;

    .text--paragraphs {
      max-width: 380px;
    }
  }
}
</style>