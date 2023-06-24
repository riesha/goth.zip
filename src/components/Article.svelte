<script>
</script>

<article>
  <slot />
</article>

<style>
  article {
    width: 80ch;
    border: 1px solid aliceblue;
    border-radius: 10px;
    padding: 0.5rem;
    height: 100ch;
  }
  article :global(h2) {
    color: black;

    background-color: aliceblue;
    border-radius: 10px;
    line-height: 0.5rem;
    font-size: 12pt;

    padding: 0.5rem 1rem;
  }
  article :global(h1) {
    font-size: 4rem;
    text-align: center;
    padding-bottom: 1rem;
    text-transform: uppercase;
  }
  article :global(h2::before) {
    content: "-//";
    margin-right: 0.5rem;
  }
</style>
