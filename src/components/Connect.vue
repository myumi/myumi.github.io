<template>
  <div id="connect">
    <a href="https://github.com/myumi">
      <IconGitHub />
    </a>
    <a href="https://linkedin.com/myumi">
      <IconLinkedIn />
    </a>
    <a href="mailto:myumiak@gmail.com">
      <IconGmail />
    </a>
  </div>
</template>

<script>
import IconLinkedIn from './icons/IconLinkedIn'
import IconGitHub from './icons/IconGitHub'
import IconGmail from './icons/IconGmail'

export default {
  name: 'Connect',
  components: { 
    IconGitHub, 
    IconGmail, 
    IconLinkedIn 
  }
}
</script>

<style lang="scss" scoped>
  #connect {
    display: flex;
    flex-direction: column;
    justify-content: space-around;

    padding: 100px 0;
    margin: 0 60px;
    width: 50px;
  }
</style>