<div class="promotion">
    <div class="promotion__main">
        <div class="promotion__main-percent">%</div>
        <h1 class="promotion__main-title">Pfirsich Eistee Ausverkauf</h1>
        <p class="promotion__main-text">
            Profitieren sie jetzt von<br>unfassbaren 5%* auf den<br>Pfirsich Eistee!
        </p>
    </div>
    <div class="promotion__wrapper">
        <div class="promotion__information">
            <p class="promotion__information-text">
                * 4,7619% auf den Preis von einem Pfirsich Eistee. Angebot gilt bis am 10. Oktober und kann jederzeit
                unbegründet zurückgezogen werden. Der QR Code für das Angebot kann bei der Verkaufsstelle gefunden
                werden.
            </p>
        </div>
        <div class="promotion__call">
            <p class="promotion__call-text">Jetzt sparen!</p>
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
      padding: 40px;
      background: linear-gradient(128deg, #3388ff 0%, hsl(0, 75%, 50%) 100%);
      color: #fff;
      text-align: left;
      border-radius: var(--border-radius);

      &-percent {
        position: absolute;
        right: 0;
        margin: -200px;
        font-size: 900px;
        font-weight: bold;
        opacity: 0.5;
      }

      &-title {
        font-size: 80px;
        margin-bottom: 20px;
      }

      &-text {
        font-weight: bold;
        font-size: 40px;
        margin-bottom: 0;
        line-height: 50px;
      }
    }

    &__wrapper {
      display: grid;
      grid-gap: 40px;
      grid-template-columns: 3fr 1fr;
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

    &__call {
      display: flex;
      align-items: center;
      padding: 0 40px;
      border-radius: var(--border-radius);
      background: #fff;

      &-text {
        text-align: left;
        font-weight: bold;
        font-size: 30px;
      }
    }
  }
</style>