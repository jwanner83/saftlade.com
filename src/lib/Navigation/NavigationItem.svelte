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
    padding: 16px 5px;
    text-align: center;
    font-weight: bold;
    font-size: 18px;
    border: none;
    border-radius: var(--border-radius-small);

    :global & + & {
      margin-left: 25px;
    }

    &--active {
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
