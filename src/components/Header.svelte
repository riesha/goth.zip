<script>
  import { onMount } from "svelte";

  let time = new Date();
  let date;

  $: date = time.toUTCString();

  onMount(() => {
    const interval = setInterval(() => {
      time = new Date();
    }, 1000);

    return () => {
      clearInterval(interval);
    };
  });
</script>

<header>
  <div class="left">
    <p>goth.zip -// {date}</p>
  </div>

  <div class="right">
    <ul>
      <li><a href="/">home</a></li>
      <li><a href="/about">about</a></li>
      <li><a href="/contact">contact</a></li>
    </ul>
  </div>
</header>

<style>
  header {
    display: flex;
    width: 80ch;
    justify-content: space-between;
    align-items: center;
    padding: 0.5rem;
    border: 1px solid aliceblue;
    border-radius: 10px;
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
  ul {
    display: flex;
    list-style: none;
    padding: 0;
    gap: 0.5rem;
  }
  ul:first-child::before {
    content: "[";
  }
  ul:last-child::after {
    content: "]";
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
