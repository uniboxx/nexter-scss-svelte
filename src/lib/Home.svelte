<script>
  import { base, icons } from '../js/constants';

  const { home } = $props();
</script>

<div class="home">
  <img
    src={`${base}/img/house-${home.id}.jpeg`}
    alt={`House ${home.id} `}
    class="home__img" />
  <svg class="home__like">
    <use xlink:href={`${icons}#icon-heart-full`}></use>
  </svg>
  <h5 class="home__name">{home.name}</h5>
  <div class="home__location">
    <svg class="">
      <use xlink:href={`${icons}#icon-map-pin`}></use>
    </svg>
    <p>{home.country}</p>
  </div>
  <div class="home__rooms">
    <svg class="">
      <use xlink:href={`${icons}#icon-profile-male`}></use>
    </svg>
    <p>{home.rooms} rooms</p>
  </div>
  <div class="home__area">
    <svg class="">
      <use xlink:href={`${icons}#icon-expand`}></use>
    </svg>
    <p>{home.size} m<sup>2</sup></p>
  </div>
  <div class="home__price">
    <svg class="">
      <use xlink:href={`${icons}#icon-key`}></use>
    </svg>
    <p>${home.price}</p>
  </div>
  <button class="btn home__btn">Contact realtor</button>
</div>

<style lang="scss">
  @use '../styles/vars';

  .home {
    background-color: vars.$color-grey-light-1;

    display: grid;
    grid-template-columns: repeat(2, 1fr);
    row-gap: 3.5rem;

    &__img {
      width: 100%;
      grid-column: 1/-1;
      grid-row: 1/2;
      z-index: 1;
    }

    &__like {
      grid-row: 1/2;
      grid-column: 2/-1;
      fill: vars.$color-primary;
      width: 2.5rem;
      height: 2.5rem;
      justify-self: end;
      margin: 1rem;
      z-index: 2;
    }

    &__name {
      grid-column: 1/-1;

      font-family: vars.$font-display;
      font-size: 1.6rem;
      text-align: center;
      padding: 1.25rem;
      background-color: vars.$color-secondary;
      color: #fff;
      font-weight: 400;
      width: 80%;
      justify-self: center;
      align-self: end;
      grid-row: 1/2;
      z-index: 3;
      transform: translateY(50%);
    }

    &__location,
    &__rooms,
    &__area,
    &__price {
      font-size: 1.5rem;
      margin-left: 2rem;
      display: flex;
      align-items: center;
      gap: 1rem;

      svg {
        fill: vars.$color-primary;
        width: 2rem;
        height: 2rem;
      }
    }

    &__location,
    &__rooms {
      margin-top: 2.5rem;
    }

    &__btn {
      grid-column: 1/-1;
    }
  }
</style>
