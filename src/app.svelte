<script>
  export let name;
  export let href = 'https://svelte.dev/tutorial';
</script>

<style>
  main {
    margin: 0 auto;
    max-width: 240px;
    padding: 1em;
    text-align: center;
  }

  h1 {
    color: #ff3e00;
    font-size: 4em;
    font-weight: 100;
    text-transform: uppercase;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the
    <a {href}>Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
</main>
