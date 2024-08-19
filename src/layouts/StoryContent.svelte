<div class="story__content">
  <h3 class="h3 heading-3 mb-sm">Happy Customers</h3>
  <h2 class="heading-2 heading-2--dark mb-md">
    &ldquo;The best decision of our lives&rdquo;
  </h2>
  <p class="story__text">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed nemo fugit
    molestias ab accusamus rem? Ab cupiditate nobis assumenda sed.
  </p>
  <button class="btn">Find your own home</button>
</div>

<style lang="scss">
  @use '../styles/vars';

  .story {
    &__content {
      background-color: vars.$color-grey-light-1;
      grid-column: col-start 5 / full-end;

      padding: 6rem 8svw;

      // display: flex;
      // flex-direction: column;
      // justify-content: center;
      // align-items: start;

      display: grid;
      align-content: center;
      justify-items: start;
      @media only screen and (max-width: vars.$bp-medium) {
        grid-column: 1/-1;
        grid-row: 5/6;
      }
    }

    &__text {
      font-size: 1.5rem;
      font-style: italic;
      margin-bottom: 4rem;
    }
  }
</style>
