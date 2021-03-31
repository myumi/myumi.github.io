<template>
  <div id="footer">
    <div className="footer--content">
      <div class="footer--left">
        <div class="footer--icon"></div>
        <div class="footer--info">
          <h1 class="footer--name">Mayumi Kalinowski</h1>
          <h2 class="footer--title">Full-stack Developer</h2>
          <div class="footer--networks">
            <Connect />
          </div>
        </div>
      </div>

      <div class="footer--right">
        <span>© 2021 Mayumi Kalinowski</span>
        <span>designed in <a>Figma</a></span>
        <span>made with <a>Vue</a></span>
      </div>
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

  #footer {
    display: flex;
    align-items: center;

    background-color: #E8E6FC;
    color: #6155C5;
    font-size: 18px;
    padding: 20px 0;
    line-height: 34px;
    width: 100vw;

    .footer--content {
      display: flex;
      flex-direction: column;

      box-sizing: border-box;
      margin: auto;
      padding: 0 40px;
      width: 100%;
      max-width: 1200px;

      @include tablet-portrait {
        flex-direction: row;
        align-items: center;
        justify-content: space-between;

        padding: 0 50px;
      }

      @include desktop {
        box-sizing: content-box;
      }

      .footer--left {
        @include tablet-portrait {
          display: flex;
          flex-direction: row;
          flex: 1 1 0;
        }

        .footer--icon {
          height: 100px;
          width: 100px;
        }

        .footer--info {

          .footer--name {
            display: block;
            font-size: 22px;

            @include tablet-portrait {
              font-size: 24px;
            }
          }

          .footer--title {
            display: block;
            font-size: 18px;
            margin: 0 0 10px;

            @include tablet-portrait {
              font-size: 18px;
            }
          }

          .footer--networks {
            margin: 10px 0 20px;

            @include tablet-portrait {
              margin: 0;
            }
          }
        }
      }

      .footer--right {
        display: flex;
        flex-direction: column;

        font-size: 14px;
        line-height: 22px;

        @include tablet-portrait {
          align-items: right;

          font-size: 16px;
          line-height: 30px;
          text-align: right;
        }

        @include desktop {
          font-size: 18px;
        }
      }
    }
  }
</style>