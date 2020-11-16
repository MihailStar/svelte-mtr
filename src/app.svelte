<script>
  const name = 'Rich Harris';
  const src = 'https://avatars0.githubusercontent.com/u/1162160';
  const html = `<div>&copy; ${name}</div>`;
</script>

<style>
  :global(.wrapper) {
    margin: 0 auto;
    max-width: 960px;
    min-width: 320px;
  }

  main {
    text-align: center;
  }
</style>

<main>
  <div class="wrapper">
    <h1>{name}</h1>
    <img {src} alt="{name}" />
    {@html html}
  </div>
</main>
