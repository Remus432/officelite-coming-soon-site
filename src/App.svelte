<script lang="ts">
  // Components
  import HeroPattern from "./components/HeroPattern.svelte"
  // Layout
  import Nav from "./layout/Nav.svelte"
  import Hero from "./layout/Hero.svelte"
  import Pricing from "./layout/Pricing.svelte"
  import Footer from "./layout/Footer.svelte"
</script>

<main>
  <HeroPattern />
  <Nav />
  <Hero />
  <Pricing />
  <Footer />
</main>

<style lang="scss" global>
  @use "./main" as *;

  main { 
    position: relative; 
    overflow-x: hidden;
  }

</style>
