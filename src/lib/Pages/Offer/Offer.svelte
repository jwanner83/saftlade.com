<script lang="ts">
</script>

<div class="offer">
    <div class="offer__item offer__item--first">
        <h3 class="offer__item-amount">NUR 1.50 CHF</h3>
    </div>
    <div class="offer__item offer__item--second">
        <h3 class="offer__item-amount">NUR 1.05 CHF</h3>
    </div>

    <div class="offer__banner-container">
        <p class="offer__banner offer__banner--first">REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL REDBULL</p>
        <p class="offer__banner offer__banner--second">ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA</p>
        <p class="offer__banner offer__banner--third">ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA ICETEA</p>
    </div>
</div>

<style lang="scss">
  .offer {
    position: relative;
    display: flex;
    gap: 50px;
    height: 500px;

    &__banner {
      transform: rotate(-10deg);
      position: absolute;
      color: #fff;
      font-weight: bold;
      font-size: 68px;
      white-space: nowrap;

      &-container {
        position: absolute;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }

    &__banner--first {
      z-index: 2;
      margin-top: -100px;
    }

    &__banner--second {
      z-index: 4;
      margin-bottom: -100px;
      clip-path: inset(0 0 0 50%);
    }

    &__banner--third {
      margin-bottom: -100px;
      clip-path: inset(0 50% 0 0);
    }

    &__item {
      position: relative;
      height: 100%;
      width: 100%;
      display: flex;
      justify-content: center;
      border-radius: var(--border-radius);

      &-amount {
        color: #fff;
        z-index: 10;
        padding: 20px;
        font-size: 22px;
      }

      &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        border-radius: var(--border-radius);
        background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, hsl(0, 0%, 11%) 100%);
      }
    }

    &__item--first {
      z-index: 1;
      background: url("https://images.unsplash.com/photo-1570526427001-9d80d114054d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=987&q=80") center center no-repeat;
      background-size: cover;
      align-items: flex-end;
    }

    &__item--second {
      z-index: 3;
      background: url("https://images.unsplash.com/photo-1561050933-2482aca2dd64?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8aWNldGVhfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=900&q=60") center center no-repeat;
      background-size: cover;
      align-items: flex-start;

      &::before {
        transform: rotate(180deg);
      }
    }
  }
</style>