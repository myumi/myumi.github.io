<template>
  <footer>
    <div class="footer__contact">
      <h1 class="footer__header">Want to get in touch?</h1>
      <p class="footer__content">
        There should be some text and content here but I'm not sure what yet.<br />
        Social networks? icons? A description? Who knows.
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
    background-color: $pink;
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
    color: $wine;
    margin: 0 0 10px;
  }

  .footer__content {
    line-height: 1.5;
  }
</style>
