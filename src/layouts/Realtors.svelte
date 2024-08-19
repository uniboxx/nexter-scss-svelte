<script>
  import Realtor from '../lib/Realtor.svelte';

  const realtors = [
    { id: 1, name: 'Erik Feiman', sold: 245 },
    { id: 2, name: 'Kim Brown', sold: 212 },
    { id: 3, name: 'Toby Ramsey', sold: 198 },
  ];
</script>

<div class="realtors">
  <h3 class="heading-3">Top 3 realtors</h3>
  <div class="realtors__list">
    {#each realtors as realtor (realtor.id)}
      <Realtor {realtor} />
    {/each}
  </div>
</div>

<style lang="scss">
  @use '../styles/vars';

  .realtors {
    background-color: vars.$color-secondary;
    grid-column: col-start 7 / full-end;
    padding: 3rem;

    display: grid;
    justify-items: center;
    align-content: center;
    row-gap: 2rem;

    &__list {
      display: grid;
      grid-template-columns: min-content max-content;
      gap: 5svh 2rem;
      align-items: center;
    }

    @media only screen and (max-width: vars.$bp-medium) {
      grid-column: 1/-1;

      &__list {
        grid-template-columns: repeat(3, min-content max-content);
      }
    }

    @media only screen and (max-width: vars.$bp-small) {
      &__list {
        grid-template-columns: min-content max-content;
      }
    }
  }
</style>
