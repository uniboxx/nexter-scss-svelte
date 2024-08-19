<script>
  import { icons } from '../js/constants';
  import Feature from '../lib/Feature.svelte';

  const features = [
    { id: 1, icon: 'global', title: "World's best luxury homes" },
    { id: 2, icon: 'trophy', title: 'Only the best properties' },
    { id: 3, icon: 'map-pin', title: 'All homes in top locations' },
    { id: 4, icon: 'key', title: 'Your home in one week' },
    { id: 5, icon: 'presentation', title: 'Top 1% realtors' },
    { id: 6, icon: 'lock', title: 'Secure payments on Nexter' },
  ];
</script>

<div class="section features">
  {#each features as feature (feature.id)}
    <Feature {feature} />
  {/each}
</div>

<style lang="scss">
  @use '../styles/vars';

  .features {
    grid-column: center-start / center-end;

    margin: 15rem 0;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
    grid-gap: 6rem;
    align-items: start;

    @media only screen and (max-width: vars.$bp-small) {
      margin: 5rem 1rem;
    }
  }
</style>
