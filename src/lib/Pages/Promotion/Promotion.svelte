<div class="promotion">
    <div class="promotion__main promotion__main--redbull">
        <div class="promotion__main-background">NEU</div>
        <h1 class="promotion__main-subtitle">NEU VERFÜGBAR</h1>
        <h1 class="promotion__main-title">Redbull</h1>
        <p class="promotion__main-text">
            Profitieren sie jetzt von einem unschlagbaren Einführungspreis.*
        </p>
    </div>
    <div class="promotion__main promotion__main--icetea">
        <div class="promotion__main-background">%</div>
        <h1 class="promotion__main-title">Eistee<br> Ausverkauf</h1>
        <p class="promotion__main-text">
            Alles muss raus! Jetzt von legendären 10%** auf den Eistee profitieren!
        </p>
    </div>
    <div class="promotion__wrapper">
        <div class="promotion__information">
            <p class="promotion__information-text">
                * Der Einführungspreis von 1.50 CHF pro Dose ist bis am 10. Oktober 2021 gültig.
            </p>
            <p class="promotion__information-text">
                ** 9,52381% auf den Preis von einem Eistee. Angebot ist bis am 12. Oktober 2021 gültig oder solange
                vorrat.
            </p>
        </div>
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
        background: linear-gradient(115deg, #452730 0%, hsl(250, 76%, 50%) 100%);

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