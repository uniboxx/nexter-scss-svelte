<script>
  import { base } from '../js/constants';
</script>

<header class="header">
  <img src={`${base}/img/logo.png`} alt="Nexter logo" class="header__logo" />
  <h3 class="heading-3">Your own home:</h3>
  <h1 class="heading-1">The ultimate personal freedom</h1>
  <button class="btn header__btn">View our properties</button>
  <div class="header__seenon-text">As seen on</div>
  <div class="header__seenon-logos">
    <img src={`${base}/img/logo-bbc.png`} alt="Seen on logo 1" />
    <img src={`${base}/img/logo-forbes.png`} alt="Seen on logo 2" />
    <img src={`${base}/img/logo-techcrunch.png`} alt="Seen on logo 3" />
    <img src={`${base}/img/logo-bi.png`} alt="Seen on logo 4" />
  </div>
</header>

<style lang="scss">
  @use '../styles/vars';

  .header {
    background-color: vars.$color-grey-dark-1;
    grid-column: full-start/ col-end 6;

    background:
      linear-gradient(
        rgba(vars.$color-secondary, 0.93),
        rgba(vars.$color-secondary, 0.93)
      ),
      url('/nexter-scss-svelte/img/hero.jpeg') center/cover;
    padding: 4rem 8rem 8rem;

    display: grid;
    grid-template-rows: 1fr min-content minmax(6rem, min-content) 1fr;
    grid-template-columns: minmax(min-content, max-content);
    row-gap: 1.5rem;
    justify-content: center;

    &__logo {
      height: 3rem;
      justify-self: center;
    }

    &__btn {
      align-self: start;
      justify-self: start;
    }

    &__seenon-text {
      display: grid;
      grid-template-columns: 1fr max-content 1fr;
      align-items: center;
      column-gap: 1.5rem;

      font-size: 1.6rem;
      color: vars.$color-grey-light-1;

      &::before,
      &::after {
        content: '';
        height: 1px;
        display: block;
        background-color: currentColor;
      }
    }

    &__seenon-logos {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      column-gap: 3rem;
      justify-items: center;
      align-items: center;

      img {
        max-height: 2.5rem;
        max-width: 100%;
        filter: brightness(70%);
      }
    }

    @media only screen and (max-width: vars.$bp-medium) {
      grid-column: 1/-1;
    }

    @media only screen and (max-width: vars.$bp-small) {
      padding: 5rem;
    }
  }
</style>
