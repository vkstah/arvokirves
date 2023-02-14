<script lang="ts">
  export let value: number;
  export let placeholder: string = "";
  export let min: number | null;
  export let max: number | null;
  export let step: number = 1;
  export let unit: string = "";
</script>

<div class="field">
  <input type="number" bind:value {min} {max} {placeholder} {step} />
  <span class="unit">{unit}</span>
</div>

<style lang="scss">
  input {
    border: none;
    outline: none;
    width: 100%;
    height: 100%;
  }

  input,
  .unit {
    background-color: inherit;
    color: var(--color-paragraph);
    font-size: 16px;
  }

  // The height of these elements must match.
  .field,
  input {
    height: 42px;
  }

  .field {
    background-color: var(--color-input);
    font-weight: 500;
    display: flex;
    align-items: center;
    border-radius: 4px;
  }

  input {
    padding-left: 1rem;
    border-top-left-radius: 4px;
    border-bottom-left-radius: 4px;
  }

  .unit {
    padding-right: 1rem;
    cursor: default;
    min-width: 60px;
    text-align: right;
  }

  input::-webkit-outer-spin-button,
  input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }
  input[type="number"] {
    -moz-appearance: textfield;
  }
</style>
