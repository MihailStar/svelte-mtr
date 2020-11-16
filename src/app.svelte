<script>
  let title = 'Svelte';
  let pos = {
    x: 0,
    y: 0,
  };
  let inputValue = '';

  function clickHandler() {
    title += '!';
  }

  function mousemoveHandler(e) {
    [pos.x, pos.y] = [e.x, e.y];
  }
</script>

<style>
  :global(body) {
    text-align: center;
  }

  div {
    background-color: #4169e1;
    height: 320px;
    margin: 0 auto;
    margin-bottom: 1em;
    width: 320px;
  }
</style>

<h1>title: {title}</h1>
<button type="button" on:click="{clickHandler}">Change title</button>

<div on:mousemove="{mousemoveHandler}">
  <h2>x: {pos.x}, y: {pos.y}</h2>
</div>

<form on:submit|preventDefault>
  <input
    type="text"
    on:input="{(e) => {
      e.preventDefault();
      inputValue = e.target.value;
    }}"
  />
  <input type="text" value="{`inputValue: ${inputValue}`}" disabled />
  <button>Submit form</button>
</form>
