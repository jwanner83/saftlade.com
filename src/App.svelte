<script lang="ts">
  import Navigation from './lib/Navigation/Navigation.svelte'
  import Section from './lib/Layout/Section.svelte'
  import Offer from './lib/Pages/Offer/Offer.svelte'
  import Promotion from './lib/Pages/Promotion/Promotion.svelte'
  import Home from './lib/Pages/Home/Home.svelte'
</script>

<main>
    <Home />
    <Navigation/>
    <div class="content">
        <Section title="Angebot">
            <Offer />
        </Section>
        <Section title="Aktion">
            <Promotion />
        </Section>
    </div>
</main>

<style>
  :root {
    --primary-light: #48A8BC29;
    --primary: #48A8BC;
    --dark-gray: #636363;
    --primary-background: #000;
    --secondary-background: #1C1C1C;
    --border-radius: 10px;
    --border-radius-small: 5px;
  }

  main {
    min-height: 100%;
    width: 100%;
    background: var(--primary-background);
    padding-bottom: 150px;
  }

  .content {
      overflow: hidden;
      min-height: 100%;
      width: 100%;
      background: var(--primary-background);
  }
</style>
