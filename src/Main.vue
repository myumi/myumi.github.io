<template>
  <main>
    <div class="main__content">
      <!-- <Navigation /> -->
      <Profile />
      <Work />
      <About />
    </div>
    <Footer />
  </main>
</template>

<script>
// import Navigation from './components/Navigation.vue'
import Profile from './components/Profile'
import Work from './components/Work'
import About from './components/About.vue'
import Footer from './components/Footer'

export default {
  name: 'Portfolio',
  components: { 
    // Navigation, 
    Profile, 
    Work, 
    About, 
    Footer,
  }
}
</script>

<style lang="scss">
  @use "./sass/main";
  @use "./sass/spacing";

  main {
    display: flex;
    flex-direction: column;
  }

  .main__content {
    @include spacing.main-spacing;
    width: 100%;
  }
</style>
