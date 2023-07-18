<script>
</script>

<footer>
  <p>
    this website is part of the <a href="https://staydown.money/"
      >staydown.money
    </a> webring
  </p>
  <ul>
    <li>
      <a href="https://staydown.money/wr?prev=https://goth.zip/">prev</a>
    </li>
    <li>
      <a href="https://staydown.money/wr?random=https://goth.zip/">random</a>
    </li>
    <li>
      <a href="https://staydown.money/wr?next=https://goth.zip/">next</a>
    </li>
  </ul>
</footer>

<style>
  footer {
    margin-block: 1rem;
    padding: 0.5rem;
    border: 1px solid aliceblue;
    border-radius: 10px;
    width: 80ch;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 1rem;
  }
  .right {
    display: flex;
    gap: 1rem;
  }
  a {
    color: var(--accent);
    text-decoration: none;
    transition: all 0.2s ease-in;
  }
  a:hover {
    color: var(--accent-deep);
  }
  ul {
    display: inherit;

    list-style: none;
    padding: 0;
  }
  li:not(:last-child)::after {
    content: "|";
    margin-inline: 0.5rem;
  }
  @media only screen and (max-width: 600px) {
    footer {
      width: 90vw;
    }

    li:not(:last-child)::after {
      margin-inline: 0.2rem;
    }
  }
</style>
