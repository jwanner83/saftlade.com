<script lang="ts">
    import { onMount } from 'svelte'
    import NavigationItem from './NavigationItem.svelte'

    let active: number = 1
    const observer: IntersectionObserver = new IntersectionObserver(onEntry, {
        threshold: 0.7
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

        <NavigationItem title="Kontakt" type="dominant" link="mailto:jonas@wanner.com?subject=Saftlade: Kontaktanfrage"/>
    </div>
</div>

<style lang="scss">
  .navigation {
    background: var(--secondary-background);
    padding: 10px;
    display: flex;
    gap: 10px;
    border-radius: var(--border-radius);
    animation: transition-in 0.6s;
    animation-delay: 1s;
    animation-fill-mode: both;

    @media (max-width: 850px) {
      padding: 5px;
      gap: 5px;
    }

    &__wrapper {
      overflow: hidden;
      z-index: 10;
      position: sticky;
      top: 0;
      width: 100%;
      display: flex;
      justify-content: center;
      padding: 40px 0;
    }
  }

  @keyframes transition-in {
    from {
      opacity: 0;
      transform: translateY(100%) scale(0.7);
    }
    to {
      opacity: 1;
      transform: translateY(0) scale(1);
    }
  }
</style>
