<script lang="ts">
  // Components
  import Button from "../components/Button.svelte"
</script>

<form class="form">
  <input type="text" placeholder="Name" class="form__field form__field--input">
  <input type="email" placeholder="Email Address" class="form__field form__field--input">
  <select class="form__field form__field--dropdown">
    <option value="Basic Pack">
      <span>Basic Pack</span>
      <span>Free</span>
    </option>
    <option value="Pro Pack">
      <span>Pro Pack</span>
      <span>$9.99</span>
    </option>
    <option value="Basic Pack">
      <span>Ultimate Pack</span>
      <span>$19.99</span>
    </option>
  </select>
  <input type="number" placeholder="Phone Number" class="form__field form__field--input">
  <input type="text" placeholder="Company" class="form__field form__field--input">
  <Button 
    content="Get on the list"
    btnType="1"
    marginTop="m--1"
  />
</form>

<style lang="scss">
  .form {
    align-items: center;
    display: flex;
    flex-direction: column;

    &__field { width: 100%; }
  }
</style>