<script lang="ts">
import { onMount } from 'svelte'

const observer: IntersectionObserver = new IntersectionObserver(onIntersect, {
    threshold: 0.6
})

function onIntersect(entries): void {
    for (const entry of entries) {
        if (entry.intersectionRatio > 0) {
            entry.target.classList.add('offer__intersect')
        }
    }
}

onMount(async () => {
    document.querySelectorAll('[data-offer-intersect]').forEach(element => {
        observer.observe(element)
    })
})
</script>

<div class="offer">
    <div class="offer__item offer__item--first" data-offer-intersect>
        <h3 class="offer__item-amount">NUR 1.95 CHF</h3>
    </div>
    <div class="offer__item offer__item--second" data-offer-intersect>
        <h3 class="offer__item-amount">NUR 0.65 CHF</h3>
    </div>

    <div class="offer__banner-container" data-offer-intersect>
        <p class="offer__banner offer__banner--first">COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO COLA ZERO</p>
        <p class="offer__banner offer__banner--second">CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN</p>
        <p class="offer__banner offer__banner--third">CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN CAPRI SUN</p>
    </div>
</div>

<style lang="scss">
  .offer {
    position: relative;
    display: flex;
    gap: 50px;
    height: 500px;

    @media (max-width: 850px) {
      height: 400px;
    }

    @media (max-width: 700px) {
      gap: 20px;
    }

    &__banner {
      opacity: 0;
      transition: 1s;
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
      transform: translateX(-80px) rotate(-10deg);
      z-index: 2;
      margin-top: -100px;

      @media (max-width: 700px) {
        margin-top: -50px;
      }
    }

    &__banner--second {
      transform: translateX(80px) rotate(-10deg);
      z-index: 4;
      margin-bottom: -100px;
      clip-path: inset(0 0 0 50%);

      @media (max-width: 700px) {
        margin-bottom: -50px;
      }
    }

    &__banner--third {
      transform: translateX(80px) rotate(-10deg);
      margin-bottom: -100px;
      clip-path: inset(0 50% 0 0);

      @media (max-width: 700px) {
        margin-bottom: -50px;
      }
    }

    &__item {
      transition: 0.8s;
      opacity: 0;
      transform: translateY(60px);
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
      background: url("/images/cola.jpg") center center no-repeat;
      background-size: cover;
      align-items: flex-end;
    }

    &__item--second {
      transition-delay: 0.3s;
      z-index: 3;
      background: url("/images/juice.jpg") center center no-repeat;
      background-size: cover;
      align-items: flex-start;

      &::before {
        transform: rotate(180deg);
      }
    }
  }

  :global .offer {
    .offer__item.offer__intersect {
      opacity: 1;
      transform: translateY(0)
    }

    .offer__banner-container.offer__intersect {
        .offer__banner {
          opacity: 1;
          transform: translateX(0) rotate(-10deg);
        }
    }
  }
</style>