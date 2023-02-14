<script>
  import { page } from "$app/stores";
</script>

<div>
  <h1>{$page.status}: {$page.error?.message}</h1>
  <p>Hups! Jokin meni pieleen. <a href="/">Palaa etusivulle?</a> 🤔</p>
</div>

<style lang="scss">
  div {
    height: 90vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  h1 {
    color: var(--color-white);
    font-size: 24px;
  }

  p {
    color: var(--color-paragraph);
    margin-top: 0.75rem;
  }

  a {
    color: var(--color-white);
  }
</style>
