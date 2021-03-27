<template>
  <div id="profile">
    <div class="info">
      <div class="text">
        <h1>Hi, I’m Mayumi.</h1>
        <h2>I’m a web developer and designer based anywhere.</h2>
        <h3>(That means I like to work remotely.)</h3>
      </div>

      <div class="buttons">
        <button class="filled">Contact Me</button>
        <button class="outlined">Download CV</button>
      </div>

      <Connect />
    </div>

    <div class="graphic">
      <img src="../assets/me.png" alt="A girl with pink hair, glasses, and a cat sitting while looking at a laptop" />
    </div>

    <div class="triangle">
      <Triangle />
    </div>
  </div>
</template>

<script>
import Connect from './Connect'
import Triangle from './svgs/Triangle'

export default {
  components: { Connect, Triangle }
}
</script>

<style lang="scss" scoped>
  @import '../sass/main.scss';

  #profile {
    display: flex;
    flex-direction: row;
    position: relative;
    padding: 0 0 0 50px;

    @include desktop {
      flex-direction: row;
      padding: 0 0 0 100px;
    }

    .info {
      width: 480px;

      .text {
        h1 {
          font-weight: 700;

          @include desktop {
            font-size: 48px;
            line-height: 58px;
          }
        }

        h2 {
          font-weight: 500;

          @include desktop {
            font-size: 36px;
            line-height: 42px;
            margin: 8px 0 20px;
          }
        }

        h3 {
          font-weight: 400;

          @include desktop {
            font-size: 18px;
            line-height: 22px;
          }
        }
      }

      .buttons {
        margin: 20px 0;

        @include desktop {
          margin: 30px 0;
        }

        button {
          border-radius: 5px;
          box-shadow: 6px 6px 20px 4px rgba(0, 0, 0, 0.05), 
              3px 3px 15px 2px rgba(0, 0, 0, 0.04), 
              1px 1px 8px 1px rgba(0, 0, 0, 0.02);
          color: $pink;
          font-size: 18px;
          font-weight: 600;
          height: 50px;
          line-height: 24px;
          width: 160px;
          display: block;

          @include desktop {
            display: inline-block;
          }

          &.filled {
            background: linear-gradient(90deg, $lavender 0%, $periwinkle 100%);
            color: $white;
            margin: 0 0 10px 0;

            @include desktop {
              margin: 0 30px 0 0;
            }
          }

          &.outlined {
            position: relative;
            box-sizing: border-box;

            color: $lavender;
            background: $white;
            border: 1px solid $periwinkle;
          }
        }
      }
    }

    .graphic {
      z-index: 1; 

      img {
        height: 450px;

        @include desktop {
          height: 580px;
        }
      }
    }

    .triangle {
      position: absolute;
      z-index: -1;
      top: -85px;
      right: 0px;
    }

}
</style>