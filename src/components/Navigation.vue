<template>
  <div id="topbar">
    <div class="icon"></div>
    <nav class="nav">
      <a href="#about">About</a>
      <a href="#work">Work</a>
      <a href="#contacts">Contacts</a>
      <a>Download CV</a>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  @import '../sass/main.scss';

  #topbar {
    display: flex;
    flex-direction: row;
    align-items: center;

    height: 80px;
    margin: 0 30px;

    .icon {
      flex: 1 1 0;
    }
    nav {
      flex: 1 1 0;
      display: flex;
      flex-direction: row;
      justify-content: flex-end;

      color: $light-grey;
      font-weight: 600;

      a {
        color: $light-grey;
        margin: 0 20px;
        text-decoration: none;
      }
    }
  }
</style>
