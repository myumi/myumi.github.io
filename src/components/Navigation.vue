<template>
  <div id="topbar">
    <nav class="nav">
      <a href="#about">About</a>
      <a href="#work">Work</a>
      <a href="#contacts">Contacts</a>
      <a href="../assets/resume.pdf">Download CV</a>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #topbar {
    display: flex;
    flex-direction: row;
    align-items: center;

    height: 80px;
    margin: 0 30px;

    nav {
      flex: 1 1 0;
      display: flex;
      flex-direction: row;
      justify-content: center;

      @include tablet-portrait {
        justify-content: flex-end;
      }

      color: $light-grey;
      font-weight: 600;

      a {
        color: $light-grey;
        margin: 0 9px;
        text-decoration: none;

        @include tablet-portrait {
          margin: 0 20px;
        }
      }
    }
  }
</style>
