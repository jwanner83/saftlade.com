<script lang="ts">
    export let title: string
    export let type: string
    export let link: string
</script>

{#if link}
    <a on:click class="navigation__item navigation__item--{type}" href="{link}">
        {title}
    </a>
{:else}
    <button on:click class="navigation__item navigation__item--{type}">
        {title}
    </button>
{/if}

<style lang="scss">
  .navigation__item {
    text-decoration: none;
    cursor: pointer;
    transition: 0.3s;
    padding: 16px 12px 12px;
    text-align: center;
    width: 200px;
    font-weight: bold;
    font-size: 18px;
    border: none;
    border-radius: var(--border-radius-small);

    &--active {
      background: var(--primary-light);
      color: var(--primary)
    }

    &--inactive {
      background: none;
      color: var(--dark-gray)
    }

    &--dominant {
      background: white;
      color: black;
    }

    &:hover {
      opacity: 0.7;
    }

    &:active {
      transform: scale(0.95);
    }
  }
</style>
