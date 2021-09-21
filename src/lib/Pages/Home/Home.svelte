<div class="home">
    <div class="home__illustration-container">
        <div class="home__illustration">
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
            <p class="home__illustration-text">SAFTLADE SAFTLADE SAFTLADE SAFTLADE SAFTLADE</p>
        </div>
    </div>
    <p class="home__text">Ihre vertrauenswürdige Quelle für erfrischende, reaktivierende, Leistungssteigerende Getränke.</p>
</div>

<style lang="scss">
    .home {
      color: white;
      height: 100vh;
      max-width: 800px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      &__label {
        display: flex;
        flex-direction: column;
        justify-content: center;
      }

      &__illustration {
        width: 300px;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-content: center;
        flex-direction: column;

        &-text {
          margin: 10px 0;
          white-space: nowrap;
          font-size: 30px;
          font-weight: bold;
          line-height: 30px;
          transform: rotate(20deg);

          &:nth-child(even) {
            margin-right: 30px;
            font-size: 60px;
          }
        }

        &-container {
          height: 50%;
          overflow: hidden;
          display: flex;
          justify-content: center;
          align-items: center;
        }
      }

      &__text {
        font-size: 20px;
        max-width: 600px;
        line-height: 30px;
        text-align: center;
        margin-top: 60px;
        font-style: italic;
      }
    }
</style>