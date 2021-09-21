<script lang="ts">
  import Navigation from './lib/Navigation/Navigation.svelte'
  import Section from './lib/Layout/Section.svelte'
  import Offer from './lib/Pages/Offer/Offer.svelte'
</script>

<main>
  <Navigation />

  <Section title="Angebot">
    <Offer />
  </Section>
  <Section title="Aktion">
    <p>deger</p>
  </Section>
</main>

<style>
  :root {
    --primary-light: #48A8BC29;
    --primary: #48A8BC;

    --dark-gray: #636363;

    --primary-background: #000;
    --secondary-background: #2B2B2B;

    --box-radius: 10px;
    --box-radius-small: 5px;
  }

  main {
    overflow: hidden;
    min-height: 100%;
    width: 100%;
    background: var(--primary-background);
  }
</style>
