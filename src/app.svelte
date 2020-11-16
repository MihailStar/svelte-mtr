<script>
  let title = 'Svelte';
  $: lowerTitle = title.toLowerCase();
  $: upperTitle = title.toUpperCase();

  let counter = 0;
  $: counterClass = counter % 2 === 0 ? 'b' : 'r';

  $: {
    console.log({ title });
    console.log({ counter });
  }

  $: if (counter === 10) {
    title = '10';
  }

  function changeTitle() {
    title += '!';
  }
</script>

<style>
  div {
    text-align: center;
  }

  button {
    min-width: 24px;
  }

  .b {
    color: #0000ff;
  }

  .r {
    color: #ff0000;
  }
</style>

<div>
  <h1>{title}</h1>
  <h2>{upperTitle}</h2>
  <h2>{lowerTitle}</h2>
  <button type="button" on:click="{changeTitle}">Change title</button>

  <p class="{counterClass}">counter: {counter}</p>
  <button
    type="button"
    on:click="{() => {
      counter -= 1;
    }}"
  >
    -
  </button>
  <button
    type="button"
    on:click="{() => {
      counter += 1;
    }}"
  >
    +
  </button>
</div>
