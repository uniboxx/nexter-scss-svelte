<script>
  import { base } from '../js/constants';

  const { item } = $props();
</script>

<figure class={`gallery__item gallery__item--${item}`}>
  <img
    src={`${base}/img/gal-${item}.jpeg`}
    alt={`Gallery image ${item}`}
    class="gallery__img" />
</figure>

<style lang="scss">
  @use '../styles/vars';

  .gallery {
    &__item {
      &--1 {
        grid-column: 1/3;
        grid-row: 1/3;
      }
      &--2 {
        grid-column: 3/6;
        grid-row: 1/4;
      }
      &--3 {
        grid-column: 6/7;
        grid-row: 1/3;
      }
      &--4 {
        grid-column: 7/9;
        grid-row: 1/3;
      }
      &--5 {
        grid-column: 1/3;
        grid-row: 3/6;
      }
      &--6 {
        grid-column: 3/5;
        grid-row: 4/6;
      }
      &--7 {
        grid-column: 5/6;
        grid-row: 4/5;
      }
      &--8 {
        grid-column: 6/8;
        grid-row: 3/5;
      }
      &--9 {
        grid-column: 8/9;
        grid-row: 3/6;
      }
      &--10 {
        grid-column: 1/2;
        grid-row: 6/8;
      }
      &--11 {
        grid-column: 2/4;
        grid-row: 6/8;
      }
      &--12 {
        grid-column: 4/5;
        grid-row: 6/8;
      }
      &--13 {
        grid-column: 5/8;
        grid-row: 5/8;
      }
      &--14 {
        grid-column: 8/9;
        grid-row: 6/8;
      }
    }
    &__img {
      width: 100%;
      height: 100%; //^ se non si mette anche l'height non funziona
      object-fit: cover; //_ questo fa la magia di mantenere le proporzioni rimanendo nella cella/e
      display: block;
    }
  }
</style>
