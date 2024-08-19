<script>
  import { base, icons } from '../js/constants';
  import { homes } from '../js/data';
  import Home from '../lib/Home.svelte';
</script>

<section class="homes">
  {#each homes as home (home.id)}
    <Home {home} />
  {/each}
</section>

<style lang="scss">
  @use '../styles/vars';

  .homes {
    grid-column: center-start / center-end;
    margin: 15rem 0;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
    grid-gap: 7rem;

    @media only screen and (max-width: vars.$bp-medium) {
      margin: 10rem 2rem;
    }
    @media only screen and (max-width: vars.$bp-small) {
      margin: 5rem 2rem;
    }
  }
</style>
