<script>
  import NumberField from "$lib/components/input/NumberField.svelte";
  import NavCard from "$lib/components/NavCard.svelte";
  import DiamondIcon from "$lib/icons/DiamondIcon.svelte";
  import GraphIcon from "$lib/icons/GraphIcon.svelte";
</script>

<svelte:head>
  <title>Arvokirves</title>
</svelte:head>

<div class="header">
  <h1>Arvokirves</h1>
  <p>
    Arvokirves on kokoelma osake- ja rahastosäästäjälle suunnattuja työkaluja. Voit käyttää
    työkaluja säästämissuunnitelmasi tekemiseen tai vaikkapa osakepoiminnan tukena.
  </p>
</div>

<div class="cards">
  <NavCard
    title="Korkoa korolle -laskuri"
    description="Laske korkoa korolle -ilmiön avulla kerrytetyt tuotot sijoituksillesi."
    link="/korkoa-korolle"
    color="blue"
  >
    <GraphIcon size="32" />
  </NavCard>
  <NavCard
    title="DCF-valuaatio"
    description="Arvioi osakkeen käypää arvoa diskontatulla kassavirta-analyysimenetelmällä."
    link="/dcf-valuaatio"
    color="green"
  >
    <DiamondIcon size="32" />
  </NavCard>
</div>

<style lang="scss">
  .header {
    margin-top: 3rem;
    margin-bottom: 4rem;

    h1 {
      color: var(--color-white);
    }

    p {
      color: var(--color-paragraph);
      max-width: 800px;
      line-height: 26px;
      margin-top: 1rem;
    }
  }

  .cards {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;

    @media (min-width: 1200px) {
      grid-template-columns: 1fr 1fr 1fr;
    }
  }
</style>
