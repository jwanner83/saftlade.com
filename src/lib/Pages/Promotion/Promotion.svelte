<div class="promotion">
    <div class="promotion__main promotion__main--redbull">
        <div class="promotion__main-background">MATE</div>
        <h1 class="promotion__main-subtitle">NEU VERFÜGBAR</h1>
        <h1 class="promotion__main-title">EL TONY MATE</h1>
        <p class="promotion__main-text">
          Des Programmierers Segen, des Schlafes Fluch.
        </p>
    </div>
</div>

<style lang="scss">
  .promotion {
    display: flex;
    flex-direction: column;
    gap: 40px;

    &__main {
      overflow: hidden;
      position: relative;
      padding: 80px 40px 40px;
      background: linear-gradient(128deg, #3388ff 0%, hsl(0, 75%, 50%) 100%);
      color: #fff;
      text-align: left;
      border-radius: var(--border-radius);

      &-background {
        position: absolute;
        right: 0;
        margin: -200px;
        font-size: 900px;
        font-weight: bold;
        opacity: 0.3;
      }

      &-subtitle {
        margin-bottom: 8px;
        margin-left: 4px;
        font-weight: lighter;
        font-size: 26px;
      }

      &-title {
        font-size: 80px;
        margin-top: 0;
        margin-bottom: 20px;
      }

      &-text {
        font-weight: bold;
        font-size: 40px;
        margin-bottom: 0;
        line-height: 50px;
      }

      &--redbull {
        background: linear-gradient(65deg, #d8ca00 0%, hsl(253, 100%, 31%) 100%);

        .promotion__main-background {
          top: 0;
          left: 0;
          margin: -8px 0 0 -230px;
          font-size: 560px;
          letter-spacing: -50px;
        }
      }

      &--icetea {
        background: linear-gradient(230deg, #1bc0ad 0%, hsl(259, 76%, 50%) 100%);
      }
    }

    &__wrapper {
      display: grid;
      grid-gap: 40px;
    }

    &__information {
      padding: 40px;
      border-radius: var(--border-radius);
      background: var(--secondary-background);

      &-text {
        text-align: left;
        color: var(--dark-gray);
      }
    }
  }
</style>