<footer class="footer">
  <ul class="nav">
    <li class="nav__item">
      <a class="nav__link" href="#">Find you dream home</a>
    </li>
    <li class="nav__item">
      <a class="nav__link" href="#">Request proposal</a>
    </li>
    <li class="nav__item">
      <a class="nav__link" href="#">Download home planner</a>
    </li>
    <li class="nav__item"><a class="nav__link" href="#">Contact us</a></li>
    <li class="nav__item">
      <a class="nav__link" href="#">Submit your property</a>
    </li>
    <li class="nav__item">
      <a class="nav__link" href="#">Come work with us!</a>
    </li>
  </ul>
  <p class="copyright">
    &copy; Copyright 2024. Made by uniboxx following the css-sass course by
    Jonas Schmedtmann.
  </p>
</footer>

<style lang="scss">
  @use '../styles/vars';

  .footer {
    background-color: vars.$color-secondary;
    grid-column: full-start/full-end;

    color: #fff;
    padding: 8rem;

    @media only screen and (max-width: vars.$bp-small) {
      padding: 5rem 2rem;
    }
  }

  .nav {
    list-style: none;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    gap: 2rem;
    align-items: center;

    &__link:link,
    &__link:visited {
      font-size: 1.4rem;
      color: inherit;
      text-decoration: none;
      font-family: vars.$font-display;
      text-transform: uppercase;
      text-align: center;
      padding: 1.5rem;
      display: block;
      transition: all 0.2s;
    }

    &__link:hover,
    &__link:active {
      background-color: rgba(#fff, 0.05);
      transform: translateY(-3px);
    }
  }

  .copyright {
    text-align: center;
    font-size: 1.4rem;
    color: vars.$color-grey-light-2;
    margin-top: 6rem;
  }
</style>
