<script>
  import ProductCards from "../components/product-cards.svelte";

</script>

<div class="theme-dark">
  <ProductCards />
</div>
<div class="theme-light">
  <ProductCards />
</div>

<style>
  /* Theming variables */
  .theme-dark {
    --color-primary: #ce0b54;
    --color-background: #333;
    --color-body: #fff;
    --color-gray: #555555;
    --border-radius-default: 0.25rem;
    --spacing-factor: 1;
    --font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  }
  
  .theme-light {
    --color-primary: #ce0b54;
    --color-background: #f5f5f5;
    --color-body: #333;
    --color-gray: #e0e0e0;
    --border-radius-default: 0.25rem;
    --spacing-factor: 2;
    --font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  }

  /* Unthemed */
  :root {
    --spacing-factor: 1;
    --spacing-1: calc(1 * var(--spacing-factor) * 1rem);
    --spacing-2: calc(1 * var(--spacing-factor) * 1.5rem);
    --spacing-3: calc(1 * var(--spacing-factor) * 2rem);
  }

  :global(body) {
    margin: 0;
    padding: 0;
  }

  :global(h3, p) {
    margin: 0;
  }
</style>
