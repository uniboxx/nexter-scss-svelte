<script>
  import { base } from '../js/constants';

  const { realtor } = $props();
  const { id, name, sold } = realtor;
</script>

<img
  src={`${base}/img/realtor-${id}.jpeg`}
  alt={`Realtor ${id}`}
  class="realtors__img" />
<div class="realtor__details">
  <h4 class="heading-4 heading-4--light">{name}</h4>
  <p class="realtors__sold">{sold} houses sold</p>
</div>

<style lang="scss">
  @use '../styles/vars';

  .realtors {
    &__img {
      width: 7rem;
      border-radius: 50%;
      display: block;
    }

    &__sold {
      text-transform: uppercase;
      color: vars.$color-grey-light-2;
      margin-top: -3px;
    }
  }
</style>
