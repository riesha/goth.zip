<script>
  import Footer from "./components/Footer.svelte";
  import Header from "./components/Header.svelte";
  import router from "page";
  import About from "./pages/About.svelte";
  import Contact from "./pages/Contact.svelte";
  import Home from "./pages/Home.svelte";
  import Error from "./pages/Error.svelte";
  let page;
  router("/", () => (page = Home));
  router("/about", () => (page = About));
  router("/contact", () => (page = Contact));
  router("/*", () => (page = Error));
  router.start();
</script>

<svelte:head>
  <title>˖⁺‧₊˚♡˚₊‧⁺˖</title>
</svelte:head>
<main>
  <Header />
  <div class="content"><svelte:component this={page} /></div>

  <Footer />
</main>

<style>

  main {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    font-family: "unifont";
    min-height: 100vh;
    min-width: 100%;
  }
  .content {
    grid-area: main;
    display: grid;
    grid-template-rows: 1;
    grid-template-columns: 1;
    flex-grow: 1;
  }
  .content > :global(*) {
    grid-row: 1;
    grid-column: 1;
  }
  @media only screen and (max-width: 600px) {main {width: 90vw;}} 
</style>
