<script>
  import { fade } from "svelte/transition";
</script>

<article in:fade={{ delay: 300 }} out:fade={{ duration: 300 }}>
  <slot />
</article>

<style>
  article {
    width: 80ch;
    border: 1px solid aliceblue;
    border-radius: 10px;
    padding: 0.5rem;
    height: 100ch;
    flex-grow: 1;
    display: flex;
    flex-direction: column;

    align-items: center;
  }
  article :global(p) {
    padding-block: 0.5rem;
  }
  article :global(h2) {
    color: black;
    width: 100%;
    background-color: aliceblue;
    border-radius: 10px;
    line-height: 0.5rem;
    font-size: 12pt;
    margin-bottom: 1rem;
    padding: 0.5rem 1rem;
  }
  article :global(h1) {
    font-size: 4rem;
    text-align: center;
    margin-bottom: 1rem;
    text-transform: uppercase;
  }
  article :global(h2::before) {
    content: "-//";
    margin-right: 0.5rem;
  }
  article :global(h3) {
    text-align: center;
    margin-bottom: 1rem;
  }

  article :global(h3::before) {
    content: "·:*¨༺ ♱";
    margin-right: 0.5rem;
  }
  article :global(h3::after) {
    content: "♱ ༻¨*:·";
    margin-left: 0.5rem;
  }
  article :global(hr) {
    color: var(--fg);
    border-top: 1px solid var(--fg);
    border-left: none;
    border-right: none;
    border-bottom: none;
    width: 70%;
  }
</style>
