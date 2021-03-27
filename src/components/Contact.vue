<template>
  <div id="contact">
    <img class="contact--image" alt="A drawing of a cat sleeping in a bed" />
    <div class="contact--info">
      <h1>Wanna say hi?</h1>
      <p>
        If you'd like to work together on something,<br />
        I'm always available via email.
      </p>

      <p>
        <span class="info--label">Send me the details at</span>
        <a href="">myumiak@gmail.com</a>
      </p>

      <p>
        <span class="info--label">Artwork by</span>
        <a href="">Paraplue Illustration</a>
        <span class="info--subtext">for my personal use</span>
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../sass/main.scss';
  #contact {
    display: flex;
    flex-direction: column;

    @include desktop {
      flex-direction: row;
      justify-content: space-between;
      padding: 0 100px;
      margin: 50px 0;
    }

    .contact--image {}

    .contact--info {
      text-align: right;
      h1 {
        display: block;
      }
      p {
        display: block;
      }
      span {
        display: block;
      }
    }
  }
</style>