<template>
  <div id="work">
    <div class="work__headers">
      <h1 class="headers__h1">Work</h1>
      <h2 class="headers__h2">These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--projects">
    </div>
  </div>
</template>

<script>

export default {
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #work {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 20px auto 0;
    min-height: 600px;

    @include tablet-portrait {
      width: 500px;
    }

    @include tablet-landscape {
      width: 1100px;
    }
  }

  .work__headers {
    width: 100%;
  }

  .headers__h1 {
    font-size: 28px;
    font-weight: 600;

    @include tablet-landscape {
      font-size: 48px;
    }
  }

  .headers__h2 {
    font-size: 22px;
    font-weight: 500;

    @include tablet-landscape {
      font-size: 24px;
    }
  }
</style>