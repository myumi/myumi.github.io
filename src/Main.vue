<template>
  <main>
    <!-- <Navigation /> -->
    <Profile />
    <Work />
    <About />
    <!-- <Contact /> -->
    <!-- <Footer /> -->
  </main>
</template>

<script>
// import Navigation from './components/Navigation.vue'
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'
import About from './components/About.vue'
// import Contact from './components/Contact.vue'
// import Footer from './components/Footer.vue'

export default {
  // contact, navigation, footer, about me, profile, work
  // todo: add blobs to about
  name: 'App',
  components: { 
    // Navigation, 
    Profile, 
    Work, 
    About, 
    // Contact, 
    // Footer 
  }
}
</script>

<style lang="scss">
  @import './sass/main.scss';

  main {
    display: flex;
    flex-direction: column;

    color: $main-text;
    height: 100%;
    padding: 40px 20px;
    margin: 0 auto;
    max-width: 1200px;
  }
</style>
