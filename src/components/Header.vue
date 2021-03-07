<template>
  <div class="header--nav">
    <a href="#profile">profile</a>
    <a href="#work">work</a>
    <a href="">resume</a>
    <a href="mailto:myumiak@gmail.com">contact</a>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
@import '../assets/main.scss';

.header--nav {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;

  a {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 22px;
    margin: 10px 20px;
    text-decoration: none;
    transition: color 1.5s ease;

    &:hover {
      transition: color 0.7s ease;
      color: $white;
    }
  }
}
</style>