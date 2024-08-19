<script>
  import { base } from '../js/constants';
</script>

<div class="story__pictures">
  <img
    src={`${base}/img/story-1.jpeg`}
    alt="Couple with new house"
    class="story__img--1" />
  <img src={`${base}/img/story-2.jpeg`} alt="New house" class="story__img--2" />
</div>

<style lang="scss">
  @use '../styles/vars';

  .story {
    &__pictures {
      background-color: vars.$color-primary;
      grid-column: full-start/ col-end 4;
      background:
        linear-gradient(
          rgba(vars.$color-primary, 0.5),
          rgba(vars.$color-primary, 0.5)
        ),
        url('/img/back.jpg') top left / cover;

      display: grid;
      grid-template-columns: repeat(6, 1fr);
      grid-template-rows: repeat(6, 1fr);

      @media only screen and (max-width: vars.$bp-medium) {
        grid-column: 1/-1;
        padding: 6rem;
        align-items: center;
        column-gap: 2rem;
      }
    }

    &__img--1 {
      width: 100%;
      grid-column: 2/-2;
      grid-row: 2/-2;
      align-self: center;
      box-shadow: 0 2rem 5rem rgba(#000, 0.1);

      @media only screen and (max-width: vars.$bp-medium) {
        grid-column: 1/5;
        grid-row: 1/-1;
      }
    }

    &__img--2 {
      width: 115%;
      grid-column: 4 / -1;
      grid-row: 4/-2;
      z-index: 10;
      box-shadow: 0 2rem 5rem rgba(#000, 0.2);

      @media only screen and (max-width: vars.$bp-medium) {
        width: 100%;
        grid-column: 4/7;
        grid-row: 1/-1;
      }
    }
  }
</style>
