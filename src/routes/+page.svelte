<script>
  import ProductCards from "../components/product-cards.svelte";
  import { PUBLIC_THEME } from '$env/static/public';

  import(`../themes/${PUBLIC_THEME}.css?inline`);
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Nanum+Myeongjo&display=swap" rel="stylesheet">
</svelte:head>

<ProductCards />
