<script>
  let title = 'Svelte';
  let isChecked = true;
  let text = '';
  let selected = '1';
  let gender = 'male';

  function bindTitle(e) {
    title = e.target.value;
  }
</script>

<style>
  div {
    text-align: center;
  }
</style>

<div>
  <h1>{title}</h1>
  <input type="text" value="{title}" on:input="{bindTitle}" />
  <input type="text" bind:value="{title}" />
  <div>title: {title}</div>

  <hr />

  <input type="checkbox" bind:checked="{isChecked}" />
  <div>isChecked: {isChecked}</div>

  <hr />

  <textarea bind:value="{text}"></textarea>
  <div style="white-space: pre-wrap">text: {text}</div>

  <hr />

  <select bind:value="{selected}">
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
  </select>
  <div>selected: {selected}</div>

  <hr />

  <input type="radio" value="male" name="gender" bind:group="{gender}" />
  <input type="radio" value="female" name="gender" bind:group="{gender}" />
  <div>gender: {gender}</div>
</div>
