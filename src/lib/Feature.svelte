<script>
  import { icons } from '../js/constants';

  const { feature } = $props();
  const { icon, title } = feature;
  const text =
    'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis, eligendi natus voluptatum cupiditate sequi doloribus.';
</script>

<div class="feature">
  <svg class="feature__icon">
    <use xlink:href={`${icons}#icon-${icon}`}></use>
  </svg>
  <h4 class="heading-4 heading-4--dark">{title}</h4>
  <p class="feature__text">
    {text}
  </p>
</div>

<style lang="scss">
  @use '../styles/vars';

  .feature {
    display: grid;
    grid-template-columns: min-content 1fr;
    align-items: center;
    row-gap: 1.5rem;
    column-gap: 2.5rem;

    &__icon {
      width: 4.5rem;
      height: 4.5rem;
      fill: vars.$color-primary;
    }

    &__text {
      font-size: 1.7rem;
      grid-column: 2;
    }
  }
</style>
