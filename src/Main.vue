<template>
  <main>
    <div class="main__content">
      <Navigation />
      <Profile />
      <Work />
      <About />
    </div>
    <!-- <Contact /> -->
    <Footer />
  </main>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'
import About from './components/About.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'Portfolio',
  components: { 
    Navigation, 
    Profile, 
    Work, 
    About, 
    Footer 
  }
}
</script>

<style lang="scss">
  @import './sass/main.scss';
  @import './sass/defaults.scss';

  main {
    display: flex;
    flex-direction: column;

    height: 100%;
  }

  .main__content {
    padding: 0 20px;
    max-width: 1200px;
    margin: 0 auto;

    @include tablet-landscape {
      padding: 0 40px;
    }
  }
</style>
