<template>
  <main>
    <Navigation />
    <Profile />
    <Work />
    <About />
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
  name: 'App',
  components: { Navigation, Profile, Work, About, Footer }
}
</script>

<style lang="scss">
  @import './sass/main.scss';

  main {
    margin: auto;
    max-width: 1200px;
  }
</style>
