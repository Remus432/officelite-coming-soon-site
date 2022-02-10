<script lang="ts">
  // Variable exports
  export let content
  // Components
  import Button from "./Button.svelte"
</script>

<article class="hero-text">
  <h1 class="hero-text__headline">{content.headline}</h1>
  <p class="hero-text__description">{content.description}</p>
  <Button 
    content="Get Started"
    btnType="1"
    marginTop="m--1" />
</article>

<style lang="scss">
  @use "../styles/mixins";
  @use "../styles/query";

  .hero-text {
    --fsize-clamped: #{clamp(var(--fsize-l), 5.3vw, var(--fsize-xxl))};
    --lheight-clamped: #{calc(var(--fsize-clamped) + .8rem)};

    margin-top: var(--spacing-xl--1);
    text-align: center;

    @include query.respond(tab) {
      margin-top: unset;
      text-align: left;
    }

    &__headline {
      @include mixins.fontStyle(var(--fsize-clamped), 700, var(--lheight-clamped));

      @include query.respond(tab) {
        width: 60%;
      }
    }

    &__description {
      color: var(--color-body-text);
      margin-top: var(--spacing-m--1);

      @include mixins.fontStyle(var(--fsize-s), 400, 2.6rem);

      @include query.respond(tab) {
        width: 59%;
      }
    }
  }
</style>