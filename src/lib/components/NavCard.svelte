<script lang="ts">
  export let title: string;
  export let description: string;
  export let link: string;
  export let color: string = "blue";
</script>

<a href={link} class={`card ${color}`}>
  <p class="title">{title}</p>
  <p class="description">{description}</p>
  <div class="icon">
    <slot />
  </div>
</a>

<style lang="scss">
  .card {
    text-decoration: none;
    color: black;
    padding: 2rem 2rem 4rem;
    display: block;
    border: 1px solid;
    border-radius: 8px;
    position: relative;
    overflow: hidden;
    display: grid;
    grid-template-columns: repeat(4, minmax(0px, 1fr));
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.03);
    }
  }

  .title,
  .description {
    grid-column: span 3 / span 3;
  }

  .title {
    font-weight: 600;
    font-size: 18px;
  }

  .description {
    color: var(--color-paragraph);
    margin-top: 1rem;
    line-height: 22px;
    font-size: 14px;
  }

  .blue {
    border-color: var(--color-blue);

    .title {
      color: var(--color-blue-light);
    }

    .icon {
      color: var(--color-blue);
    }
  }

  .green {
    border-color: var(--color-green-dark);

    .title {
      color: var(--color-green-light);
    }

    .icon {
      color: var(--color-green-dark);
    }
  }

  .icon {
    position: absolute;
    bottom: -1.25rem;
    right: -1.25rem;
    border: 1px solid;
    border-radius: 50%;
    width: 6rem;
    height: 6rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
