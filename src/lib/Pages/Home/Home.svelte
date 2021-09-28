<div class="home">
    <div class="home__section home__section--first">
        <div class="home__image"></div>
    </div>
    <div class="home__section home__section--second">
        <div class="home__animation">
            <img class="home__logo" src="logo.png" alt="saftlade.com logo">
            <p class="home__text">
                Ihre vertrauenswürdige Quelle für erfrischende, reaktivierende und leistungssteigerende
                Getränke.
            </p>
        </div>
    </div>
</div>

<style lang="scss">
  .home {
    color: white;
    height: 92vh;

    &__section {
      position: relative;

      &--first {
        height: 70%;
        padding: 150px 200px 0;

        @media (max-width: 1000px) {
          padding: 100px 150px 0;
        }

        @media (max-width: 750px) {
          padding: 100px 100px 0;
        }

        @media (max-width: 600px) {
          padding: 0;
          height: 75%;
        }
      }

      &--second {
        margin-top: -130px;
        display: flex;
        align-items: center;
        flex-direction: column;
        text-align: center;
        overflow: hidden;
        padding: 0 50px;

        @media (max-width: 1200px) {
          margin-top: -120px;
        }

        @media (max-width: 750px) {
          margin-top: -95px;
        }
      }
    }

    &__image {
      border-radius: var(--border-radius);
      height: 100%;
      width: 100%;
      background: url("images/hero.jpg") center center no-repeat;
      background-size: cover;
      animation: transition-in 0.8s;
      animation-fill-mode: both;

      @media (max-width: 600px) {
        border-radius: 0;
      }
    }

    &__logo {
      margin-left: -80px;
      width: 650px;

      @media (max-width: 1200px) {
        margin-left: -65px;
        width: 570px;
      }

      @media (max-width: 750px) {
        margin-left: -56px;
        width: 450px;
      }
    }

    &__text {
      max-width: 600px;
      font-size: 26px;
      line-height: 30px;

      @media (max-width: 750px) {
        font-size: 22px;
      }

      @media (max-width: 600px) {
        font-size: 20px;
      }
    }

    &__animation {
      animation: transition-text-in 600ms;
      animation-delay: 0.3s;
      animation-fill-mode: both;
    }
  }

  @keyframes transition-in {
    from {
      opacity: 0;
      transform: scale(0.7);
      height: 0;
    }
    to {
      opacity: 1;
      transform: scale(1);
      height: 100%;
    }
  }

  @keyframes transition-text-in {
    from {
      opacity: 0;
      transform: translateY(-150px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>