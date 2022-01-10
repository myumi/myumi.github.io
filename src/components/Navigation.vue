<template>
  <div id="topbar">
    <nav class="nav">
      <span>Mayumi A. O.</span>
      <a href="#about">About</a>
      <a href="#work">Work</a>
      <a href="#contact">Contact</a>
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
    font-size: 18px;
    font-weight: bold;
    margin: auto;
    max-width: 1200px;

    @include tablet-portrait {
      margin: 0;
    }

    nav {
      flex: 1 1 0;
      display: flex;
      flex-direction: row;

      @include tablet-portrait {
        justify-content: flex-start;
      }

      color: #FF7DAD;
      font-weight: 600;

      a, span {
        color: #FF7DAD;
        text-decoration: none;
        transition: all .5s ease-in-out;

        &:first-child {
          margin: 0 10px 0 0;
        }

        &:last-child {
          margin: 0 0 0 10px;
        }

        &:not(:first-child):not(:last-child) {
          margin: 0 10px;
        }

        &:hover:not(:first-child) {
          color: #ffa8c8;
          transform: scale(1.2);
        }
      }
    }
  }
</style>
