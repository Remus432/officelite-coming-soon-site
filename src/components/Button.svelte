<script lang="ts">
  export let content: string
  export let btnType: string
  export let marginTop: string
</script>

<button class="btn btn--{btnType} {marginTop}">
  {content}
</button>

<style lang="scss">
  @use "../styles/mixins";

  .btn {
    border: none;
    border-radius: 2.8rem;
    cursor: pointer;
    padding: 1.4rem 4rem;

    @include mixins.fontStyle(var(--fsize-s), 700, 2.8rem);

    &--1 {
      background-color: var(--color-accent);
      box-shadow: 0 2.5rem 2.5rem -1rem rgba(#3F5BC2, .24);
      color: #fff;
    }

    &--2 {
      background-color: #E4EAFF;
      color: var(--color-accent);
    }

    &--3 {
      background-color: #fff;
      color: var(--color-accent);
    }
  }
</style>