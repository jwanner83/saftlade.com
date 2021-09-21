<script lang="ts">
    export let title: string
</script>

<div class="section">
    <div id="{title.toLowerCase()}" data-section>
        <h1 class="section__title">{title}</h1>

        <div class="section__content">
            <slot></slot>
        </div>
    </div>
</div>

<style lang="scss">
  .section {
    padding: 0 80px 80px;
    max-width: 800px;
    margin: 0 auto;
    text-align: center;

    &__title {
      padding-top: 200px;
      margin-top: 0;
      color: white;
      font-size: 50px;
      margin-bottom: 150px;
    }
  }
</style>