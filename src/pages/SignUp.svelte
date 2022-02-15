<script lang="ts">
  // Components
  import HeroPattern from "../components/HeroPattern.svelte"
  import Nav from "../layout/Nav.svelte"
  import HeroText from "../components/HeroText.svelte"
  import Countdown from "../components/Countdown.svelte"
  import SignUpForm from "../components/SignUpForm.svelte"

  const text = {
    headline: "Work smarter. Save time.",
    description: "Easily manage your projects. Get on the list and receive in-app perks available only to early subscribers. We are moving into final development and getting ready for official launch soon."
  }
</script>

<div class="sign-up">
  <HeroPattern />
  <Nav />
  <HeroText hideBtn={true} content={text} />
  <Countdown theme={"light"} />
  <SignUpForm />
</div>

<style lang="scss" global>
  @use "../styles/query";

  .sign-up {
    padding-inline: var(--spacing-m--1);

    .countdown { margin-top: var(--spacing-xl--1); }
    .form { margin-top: var(--spacing-xl--1); }

    @include query.respond(tab) {
      .hero-pattern { display: none!important; }
      .hero-text { text-align: center!important; }
    }
    
  }
</style>