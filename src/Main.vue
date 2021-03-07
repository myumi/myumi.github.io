<template>
  <Header />
  <Profile />
  <Work />
</template>

<script>
import Header from './components/Header.vue'
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'

export default {
  name: 'App',
  components: { Header, Profile, Work }
}
</script>

<style lang="scss">
@import './assets/main.scss';
</style>
