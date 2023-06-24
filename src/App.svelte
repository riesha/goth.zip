<script>
  import Footer from "./components/Footer.svelte";
  import Header from "./components/Header.svelte";
  import router from "page";
  import About from "./pages/About.svelte";
  import Contact from "./pages/Contact.svelte";
  import Home from "./pages/Home.svelte";
  let page;
  router("/", () => (page = Home));
  router("/about", () => (page = About));
  router("/contact", () => (page = Contact));
  router.start();
</script>

<svelte:head>
  <title>goth.zip</title>
</svelte:head>
<main>
  <Header />
  <svelte:component this={page} />
  <Footer />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    font-family: "unifont";
  }
</style>
