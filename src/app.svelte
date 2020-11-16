<script>
  let title = 'Svelte';

  function isValid(string) {
    return !(string.length < 5 || string.length > 10);
  }

  $: hasError = !isValid(title);
</script>

<style>
  div {
    text-align: center;
  }

  .with-error {
    background-color: #b22222;
    color: #f5f5f5;
  }
</style>

<div>
  <h1>{title} app</h1>
  <input class:with-error="{hasError}" type="text" bind:value="{title}" />
  {#if title.length < 5}
    <p>less 5</p>
  {:else if title.length > 10}
    <p>more 10</p>
  {:else}
    <p>norm {title.length}</p>
  {/if}
</div>
