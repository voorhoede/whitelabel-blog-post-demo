<script>
  import ProductCards from "../components/product-cards.svelte";

</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Nanum+Myeongjo&display=swap" rel="stylesheet">
</svelte:head>

<div class="theme-dark">
  <ProductCards />
</div>
<div class="theme-light">
  <ProductCards />
</div>

<style>
  /* Theming variables */
  .theme-dark {
    --color-primary: #05a993;
    --color-background: #fdfdfd;
    --color-body: #333;
    --color-gray: #f3f3f3;
    --color-gray-contrast: #333;
    --border-radius: 1rem;
    --font-family: 'Nanum Myeongjo', serif;
    --spacing-factor: 2;
    --shadow: -4px 10px 20px 0px rgb(0, 0, 0, .1);
  }
  
  .theme-light {
    --color-primary: #ce0b54;
    --color-background: none;
    --color-body: #333;
    --color-gray: none;
    --color-gray-contrast: var(--color-body);
    --border-radius: 0;
    --spacing-factor: 1;
    --font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    --shadow: none;
  }

  /* Unthemed */
  :root {
    --spacing-factor: 1;
  }

  :global(body) {
    margin: 0;
    padding: 0;
  }

  :global(h3, p) {
    margin: 0;
  }
</style>
