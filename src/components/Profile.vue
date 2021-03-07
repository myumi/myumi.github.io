<template>
  <div id="#profile">
    <div class="profile--header">
      <h1>Hi. I'm Mayumi.</h1>
      <h2>I'm a web developer and designer based anywhere.</h2>
      <h3>(That means I like to work remotely.)</h3>
    </div>
    <div class="profile--description">
      <Connect />
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
        <div class="text--image">
          <img class="image--artwork" alt="A girl with pink hair sitting cross-legged with a laptop and cat on her lap" src="../assets/me.png">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Connect from './Connect.vue'

export default {
  components: { Connect }
}
</script>

<style lang="scss" scoped>
@import '../assets/main.scss';
.profile--header {
  color: #3F3B40;
  margin: 50px 0 0 120px;
  h1 {
    font-size: 48px;
    line-height: 58px;
    margin: 0 0 5px;
    font-weight: 600;
  }
  h2 {
    font-size: 36px;
    line-height: 43px;
    width: 630px;
    margin: 0 0 20px;
  }
  h3 {
    color: #765483;
    font-size: 18px;
    line-height: 22px;
  }
}
.profile--description {
  display: flex;
  flex-direction: row;

  margin: 10vh 0 0;

  .profile--text {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $white;
    border-radius: 8px;
    font-size: 18px;
    line-height: 34px;
    padding: 48px 65px;
    width: 100%;

    .text--paragraphs {
      flex: 1 1 0;
      max-width: 420px;
    }
    .text--image {
      flex: 1 1 0;
      .image--artwork {
        position: absolute;
        top: 40px;
        right: 0;
        height: 878px;
      }
    }
  }
}
</style>