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
    --color-primary: #0dc5ad;
    --color-background-1: #fdfdfd;
    --color-background-1-contrast: #333;
    --color-background-2: #03473e;
    --color-background-2-contrast: #fff;
    --border-radius: 1rem;
    --font-family: 'Nanum Myeongjo', serif;
    --spacing-factor: 2;
    --shadow-default: -4px 10px 20px 0px #01393185;
  }
  
  .theme-light {
    --color-primary: #ce0b54;
    --color-background-1: none;
    --color-background-1-contrast: #333;
    --color-background-2: var(--color-background-1);
    --color-background-2-contrast: var(--color-background-1-contrast);
    --border-radius: 0;
    --spacing-factor: 1;
    --font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    --shadow-default: none;
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
