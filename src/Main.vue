<template>
  <main>
    <Navigation />
    <Profile />
    <Work />
    <Footer />
  </main>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: { Navigation, Profile, Work, Footer }
}
</script>

<style lang="scss">
  @import './sass/main.scss';

  main {
    margin: auto;
    max-width: 1540px;
  }
</style>
