<template>
  <div id="footer">
    <div class="left">
      <div class="icon"></div>
      <div class="info">
        <h1 class="name">Mayumi Kalinowski</h1>
        <h2 class="title">Full-stack Developer</h2>
        <div class="networks">

        </div>
      </div>
    </div>

    <div class="right">
      <span>© 2021 Mayumi Kalinowski</span>
      <span>designed in <a>Figma</a></span>
      <span>made with <a>Vue</a></span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  #footer {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    background-color: #E8E6FC;
    color: #6155C5;
    font-size: 18px;
    height: 200px;
    line-height: 34px;
    padding: 20px;
    width: 100%;
  }
  .left {

  }
  .right {
    span {
      display: block;
      text-align: right;
    }
  }
</style>