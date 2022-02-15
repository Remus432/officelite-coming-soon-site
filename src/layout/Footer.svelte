<script lang="ts">
  // Components
  import Countdown from "../components/Countdown.svelte"
  import Button from "../components/Button.svelte"
</script>

<footer class="footer-section">
  <Countdown theme={"dark"} />
  <Button 
    content="Get Started"
    btnType="1"
    marginTop="l--2" />
</footer>

<style lang="scss">
  @use "../styles/mixins";
  @use "../styles/query";

  .footer-section {
    background-color: var(--color-footer-bg);
    background-image: url("/src/assets/home/bg-footer.svg");
    background-size: cover;
    background-position: center -170vw;
    background-repeat: no-repeat;
    padding: 10rem 2.3rem;

    @include query.respond(tab) {
      background-size: 90%;
      background-position: center -110vw;;
    }

    @include mixins.flexColCenter;
  }
</style>