<script lang="ts">
    import NavigationItem from './NavigationItem.svelte'

    let active: number = 1

    function setActive(index: number): void {
        active = index
    }

</script>

<div class="navigation__wrapper">
    <div class="navigation">
        <NavigationItem title="Angebot"
                        type="{active === 1 ? 'active' : 'inactive'}"
                        link="angebot"
                        on:click={() => setActive(1)}
        />
        <NavigationItem title="Aktion"
                        type="{active === 2 ? 'active' : 'inactive'}"
                        link="aktion"
                        on:click={() => setActive(2)}
        />

        <NavigationItem title="Kontakt" type="dominant"/>
    </div>
</div>

<style lang="scss">
  .navigation {
    background: var(--secondary-background);
    padding: 10px;
    display: flex;
    gap: 10px;
    border-radius: var(--box-radius);

    &__wrapper {
      z-index: 10;
      position: fixed;
      top: 0;
      width: 100%;
      display: flex;
      justify-content: center;
      padding: 40px 0;
    }
  }
</style>
