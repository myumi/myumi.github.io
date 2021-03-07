<template>
  <div id="work">
    <div class="work--headers">
      <h1>Work</h1>
      <h2>These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--circle"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: 'AC Patterns',
          subheader: '',
          description: '',
          image: '',
        },
        {
          name: 'Vibrant: Emotional Health',
          subheader: '',
          description: '',
          image: '',
        },
        {
          name: 'Novamei',
          subheader: '',
          description: '',
          image: '',
        },
      ]
    }
  }
}
</script>

<style lang="scss">
  .work--headers {
    text-align: center;
    h1 {
      font-size: 48px;
      font-weight: 600;
      line-height: 58px;
      margin: 80px 0 0;
    }
  }
</style>