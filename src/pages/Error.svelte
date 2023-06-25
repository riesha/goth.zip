<script>
  import Article from "../components/Article.svelte";
</script>

<Article>
  <div class="center">
    <h1>AN ERROR HAS OCCURED</h1>
    <a href="/">[ home ]</a>
  </div>
</Article>

<style>
  .center {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    height: 100%;
  }
  a {
    color: var(--accent);
    text-decoration: none;
    transition: all 0.2s ease-in;
  }
  a:hover {
    color: var(--accent-deep);
  }
</style>
