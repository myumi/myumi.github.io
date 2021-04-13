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

      <div class="connect">
        <Connect />
      </div>
    </div>

    <div class="graphic">
      <img src="../assets/me.png" alt="A girl with pink hair, glasses, and a cat sitting while looking at a laptop" />
    </div>
  </div>
</template>

<script>
import Connect from './Connect'

export default {
  components: { Connect }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #profile {
    display: flex;
    flex-direction: column;

    color: $dark-grey;
    padding: 10px 40px;
    margin: auto;
    max-width: 1200px;

    @include tablet-portrait {
      flex-direction: row;
      justify-content: space-between;

      padding: 30px 50px;
    }

    .info {
      margin: 0 0 10px;

      @include tablet-portrait {
        margin: unset;
      }

      .text {
        h1 {
          font-weight: 600;

          @include desktop {
            font-size: 48px;
          }
        }

        h2 {
          font-weight: 500;

          @include tablet-portrait {
            max-width: 350px;
          }

          @include desktop {
            font-size: 36px;
            max-width: 550px;
          }
        }

        h3 {
          font-size: 16px;
          font-weight: 500;
          margin: 10px 0 0;

          @include tablet-portrait {
            font-weight: 18px;
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
          color: $pink;
          font-size: 18px;
          font-weight: 600;
          height: 50px;
          width: 130px;
          line-height: 24px;

          @include tablet-portrait {
            width: 160px;
          }

          &.filled {
            background: linear-gradient(90deg, $lavender 0%, $periwinkle 100%);
            color: $white;
            margin: 0 10px 0 0;

            @include tablet-portrait {
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

      .connect {
        display: none;

        @include tablet-portrait {
          display: unset;
        }
      }
    }

    .graphic {
      img {
        height: 350px;

        @include tablet-portrait {
          height: 350px;
        }

        @include desktop {
          height: 550px;
        }
      }
    }
  }
</style>