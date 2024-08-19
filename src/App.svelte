<script lang="ts">
  import Features from './layouts/Features.svelte';
  import Footer from './layouts/Footer.svelte';
  import Gallery from './layouts/Gallery.svelte';
  import Header from './layouts/Header.svelte';
  import Homes from './layouts/Homes.svelte';
  import Realtors from './layouts/Realtors.svelte';
  import Sidebar from './layouts/Sidebar.svelte';
  import StoryContent from './layouts/StoryContent.svelte';
  import StoryPictures from './layouts/StoryPictures.svelte';
</script>

<div class="container">
  <Sidebar />
  <Header />
  <Realtors />
  <Features />
  <StoryPictures />
  <StoryContent />
  <Homes />
  <Gallery />
  <Footer />
</div>

<style lang="scss">
  @use './styles/vars';

  .container {
    display: grid;
    grid-template-rows: 80svh min-content 40svw repeat(3, min-content);
    grid-template-columns:
      [sidebar-start] 8rem [sidebar-end full-start] minmax(6rem, 1fr)
      [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
      [center-end] minmax(6rem, 1fr) [full-end];

    // & > * {
    //   font-size: 3rem;
    //   padding: 4rem;
    // }

    @media only screen and (max-width: vars.$bp-large) {
      grid-template-rows: 6rem 80svh min-content 40svw repeat(3, min-content);
      grid-template-columns:
        [full-start] minmax(6rem, 1fr) [center-start] repeat(
          8,
          [col-start] minmax(min-content, 14rem) [col-end]
        )
        [center-end] minmax(6rem, 1fr) [full-end];
    }
    @media only screen and (max-width: vars.$bp-medium) {
      grid-template-rows: 6rem calc(100svh - 6rem);
    }
  }
</style>
