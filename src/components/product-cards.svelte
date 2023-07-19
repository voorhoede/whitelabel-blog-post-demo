<script>
  import products from '../data/products.js';
</script>

<section class="root">
  <div class="content">
    <h2 class="title">New items</h2>
    <ul class="list">
      {#each products as product}
        <li key={product.id} class="item">
          <div class="image-wrapper">
            <img src={product.images[0]} alt={product.title} class="image" />
          </div>
          <div class="item-body">
            <h3 class="item-title">{product.title}</h3>
            <p>€{product.price}</p>
          </div>
        </li>
      {/each}
    </ul>
  </div>
</section>

<style scoped>
  .root {
    --spacing-1: calc(1 * var(--spacing-factor) * 1rem);
    --spacing-2: calc(1 * var(--spacing-factor) * 1.5rem);
    --spacing-3: calc(1 * var(--spacing-factor) * 2rem);

    padding: var(--spacing-2) 0;
    background-color: var(--color-background-1);
    color: var(--color-background-1-contrast);
    font-family: var(--font-family);
  }
  
  .content {
    margin: 0 auto;
    max-width: 1200px;
  }

  .title {
    margin-top: 0;
    margin-bottom: var(--spacing-2);
  }

  .list {
    padding: 0;
    list-style: none;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--spacing-2);
    width: 100%;
  }

  @media (min-width: 720px) {
    .list {
      grid-template-columns: repeat(3, 1fr);
    }
  }
  
  @media (min-width: 968px) {
    .list {
      grid-template-columns: repeat(4, 1fr);
    }
  }

  .item {
    display: block;
    width: 100%;
    color: var(--color-body);
    background-color: var(--color-background-2);
    color: var(--color-background-2-contrast);
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: var(--shadow-default);
  }

  .image-wrapper {
    aspect-ratio: 3 / 4;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .image {
    max-width: 100%;
    max-height: 60%;
  }

  .item-body {
    padding: var(--spacing-1);
    display: flex;
    flex-direction: column;
    gap: var(--spacing-1);
  }

  .item-title {
    margin: 0;
    color: var(--color-primary);
  }
</style>
