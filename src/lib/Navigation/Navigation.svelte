<script lang="ts">
    import { onMount } from 'svelte'
    import NavigationItem from './NavigationItem.svelte'

    let active: number = 1
    const observer: IntersectionObserver = new IntersectionObserver(onEntry, {
        threshold: 0.5
    })

    function setActive(index: number): void {
        active = index
    }

    function onEntry(entry): void {
        setActive(entry[0].target.id === 'angebot' ? 1 : 2)
    }

    onMount(async () => {
        document.querySelectorAll('[data-section]').forEach(element => {
            observer.observe(element)
        })
    })
</script>

<div class="navigation__wrapper">
    <img class="navigation__favicon" src="favicon.png" alt="favicon">
    <div class="navigation">
        <NavigationItem title="Angebot"
                        type="{active === 1 ? 'active' : 'inactive'}"
                        link="#angebot"
                        on:click={() => setActive(1)}
        />
        <NavigationItem title="Aktion"
                        type="{active === 2 ? 'active' : 'inactive'}"
                        link="#aktion"
                        on:click={() => setActive(2)}
        />
    </div>
</div>

<style lang="scss">
  .navigation {
    display: flex;
    align-items: center;
    animation: transition-in 0.6s;
    animation-delay: 1s;
    animation-fill-mode: both;

    &__favicon {
      height: 100%;
      width: 50px;
      animation: transition-in 0.6s;
      animation-delay: 0.8s;
      animation-fill-mode: both;
    }

    &__wrapper {
      overflow: hidden;
      z-index: 10;
      position: sticky;
      top: 40px;
      width: 100%;
      display: flex;
      justify-content: space-between;
      padding: 0 80px;
      max-width: 800px;
      margin: 80px auto;
      text-align: center;
    }
  }

  @keyframes transition-in {
    from {
      opacity: 0;
      transform: translateY(-200%);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>
