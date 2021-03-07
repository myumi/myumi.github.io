<template>
  <Profile />
  <Work />
</template>

<script>
import Profile from './components/Profile.vue'
import Work from './components/Work.vue'

export default {
  name: 'App',
  components: { Profile, Work }
}
</script>

<style lang="scss">
@import './assets/main.scss';
</style>
