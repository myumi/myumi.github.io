<template>
  <footer id="contact">
    <div class="footer__contact">
      <h1 class="footer__header">Want to get in touch?</h1>
      <p class="footer__content">
        Please send me an email at <a href="mailto:me@mayumi.dev">me@mayumi.dev.</a><br />
        Artwork is done by the lovely <a href="https://www.paraplue-illustration.com/">Paraplü Illustration</a>, for my personal use only.<br />
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
  @use "../sass/breakpoints";
  @use "../sass/colors";
  @use "../sass/fonts";
  @use "../sass/spacing";

  footer {
    background-color: colors.$highlight;
    min-height: 100px;

    @include spacing.footer-spacing;
  }

  .footer__contact {

    @include breakpoints.desktop {
      margin: 0 auto;
      max-width: spacing.$max-width;
    }
  }

  .footer__header {
    color: colors.$large-header;
    font-size: fonts.$font-size-7;

    @include breakpoints.tablet-portrait {
      font-size: fonts.$font-size-8;
    }

    @include spacing.header-spacing;
  }

  .footer__content {
    line-height: fonts.$font-size-8;

    a {
      color: colors.$paragraph;
      text-decoration: underline;
    }
  }
</style>
