<script lang="ts">
  // Exports
  export let info: any
  export let isProPack
  // Components
  import Button from "./Button.svelte"
</script>

<article class="pricing-card {isProPack ? "pro" : ""}">
  <h2 class="pricing-pack">{info.package}</h2>
  <div class="pricing-option">
    <p class="pricing-option__price">{info.price}</p>
    <p class="pricing-option__billing">
      {info.billing}
    </p>
  </div>
  <ul class="pricing-features">
    {#each info.features as feature}
      <li class="pricing-features__item">{feature}</li>
    {/each}
  </ul>
  <Button 
    content="Try for Free"
    btnType={isProPack ? "3" : "2"}
    marginTop="m--2" />  
</article>

<style lang="scss">
  @use "../styles/mixins";

  .pricing-card {
    background-color: #fff;
    box-shadow: 0 5rem 5rem -2.5rem rgba(#4B5C9A, .1);
    border-radius: 1.3rem;
    padding: var(--spacing-l--1) 0;
    text-align: center;

    @include mixins.flexColCenter;

    &.pro {
      background-color: var(--color-accent);
      background-image: url("src/assets/home/bg-pattern-pricing.svg");
      background-size: 226%;
      background-position: center -75vw;
      background-repeat: no-repeat;

      
      & p, h2, li { color: #fff; }
    }
  }

  .pricing-pack {
    color: var(--color-headline);

    @include mixins.fontStyle(var(--fsize-m), 700, 2.8rem);
  }

  .pricing-option {
    margin-top: var(--spacing-l--1);

    &__price {
      @include mixins.fontStyle(var(--fsize-xxl), 700, 6.4rem);
    }

    &__billing {
      color: var(--color-headline);
      margin-top: .8rem;
      line-height: 2.8rem;
    }
  }

  .pricing-features {
    margin-top: var(--spacing-l--2);

    &__item {
      color: var(--color-body-text);
      list-style: none;

      @include mixins.fontStyle(var(--fsize-s), 400, 2.8rem);

      &:not(:first-of-type) {
        margin-top: var(--spacing-s--1);
      }
    }
  }
</style>