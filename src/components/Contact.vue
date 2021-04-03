<template>
  <div id="contact">
    <img class="contact--image" alt="A drawing of a cat sleeping in a bed" />
    <div class="contact--info">
      <h1 class="contact--header">Wanna say hi?</h1>
      <p class="contact--info">
        If you'd like to work together on something, 
        I'm always available via email.
      </p>
      <p class="contact--email">
        <span class="info--label">Send me the details at</span>
        <a href="mailto:myumiak@gmail.com">myumiak@gmail.com</a>
      </p>
      <p class="contact--artwork">
        <span class="info--label">Artwork by</span>
        <a href="https://www.paraplue-illustration.com/">Paraplue Illustration</a>
        <span class="info--subtext">for my personal use</span>
      </p>
    </div>
  </div>
</template>

<style lang="scss">
@import '../sass/main.scss';

  #contact {
    display: flex;
    flex-direction: column;

    color: $dark-grey;
    padding: 40px;
    margin: auto;
    max-width: 1200px;

    @include tablet-portrait {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;

      padding: 30px 50px;
    }

    .contact--info {
      text-align: right;

      .contact--header {
        display: block;
        padding: 12px 0;
      }

      .contact--info, .contact--email, .contact--artwork {
        display: block;
        padding: 12px 0;

        a {
          color: $light-grey;

          &:hover {
            color: $dark-lavender;
          }
        }

        span {
          display: block;
          font-size: 14px;
        }
      }

      .contact--info {
        max-width: 320px;
      }

    }
  }
</style>