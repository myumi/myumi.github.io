<template>
  <Profile />
  <Work />
  <Footer />
</template>

<script>
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: { Profile, Work, Footer }
}
</script>

<style lang="scss">
  @import './sass/main.scss';
</style>
