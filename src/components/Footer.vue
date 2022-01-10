<template>
  <footer id="contact">
    <div class="footer__contact">
      <h1 class="footer__header">Want to get in touch?</h1>
      <p class="footer__content">
        Please send me an email at <a href="mailto:me@mayumi.dev">me@mayumi.dev.</a><br />
        Artwork is done by the lovely <a href="https://www.paraplue-illustration.com/">Paraplue Illustration</a>, for my personal use only.<br />
        Website is designed by me and <a href="https://github.com/myumi/portfolio/">built in Vue</a>.
      </p>
    </div>
  </footer>
</template>

<script>

export default {
  name: 'Footer'
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  footer {
    background-color: $highlight;
    max-width: unset;
    min-height: 100px;
    padding: 40px 20px;
    width: 100%;

    @include tablet-landscape {
      padding: 40px;
    }
  }

  .footer__contact {
    margin: 0 auto;
    max-width: 1100px;
  }

  .footer__header {
    color: $large-header;
    margin: 0 0 10px;
  }

  .footer__content {
    line-height: 1.8;

    a {
      color: $paragraph;

      &:hover {
        text-decoration: underline;
      }
    }
  }
</style>
