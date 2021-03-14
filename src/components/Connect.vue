<template>
  <div id="connect">
    <div class="connect--icon">
      <a href="https://github.com/myumi">
        <IconGitHub class="icon" />
      </a>
    </div>
    <div class="connect--icon">
      <a href="https://linkedin.com/myumi">
        <IconLinkedIn class="icon" />
      </a>
    </div>
    <div class="connect--icon">
      <a href="mailto:myumiak@gmail.com">
        <IconGmail class="icon" />
      </a>
    </div>
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
@import '../sass/main.scss';

  #connect {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 210px;

    .connect--icon {
      background: $periwinkle;
      border-radius: 100%;
      box-shadow: 6px 6px 20px 4px rgba(0, 0, 0, 0.05), 
          3px 3px 15px 2px rgba(0, 0, 0, 0.04), 
          1px 1px 8px 1px rgba(0, 0, 0, 0.02);
      height: 30px;
      padding: 10px;
      width: 30px;
    }
  }
</style>