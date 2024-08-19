<script>
  import GalleryItem from '../lib/GalleryItem.svelte';

  const imageNum = 14;
</script>

<section class="gallery">
  {#each new Array(imageNum) as item, idx (idx)}
    <GalleryItem item={idx + 1} />
  {/each}
</section>

<style lang="scss">
  @use '../styles/vars';

  .gallery {
    grid-column: full-start/full-end;

    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(7, 5vw);
    gap: 1.5rem;
    padding: 1.5rem;
  }
</style>
