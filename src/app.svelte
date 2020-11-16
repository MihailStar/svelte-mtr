<script>
  import Person from './person.svelte';

  let persons = [
    { id: 1, name: 'Максим', age: 20, job: 'Frontend' },
    { id: 2, name: 'Елена', age: 20, job: 'Design' },
    { id: 3, name: 'Игорь', age: 20, job: 'Backend' },
  ];

  let value = '';

  function addPerson() {
    persons = persons.concat({
      id: Date.now(),
      name: value,
    });

    // persons = [
    //   ...persons,
    //   {
    //     id: Date.now(),
    //     name: value,
    //   },
    // ];

    value = '';
  }

  function removeFirstPerson() {
    persons = persons.slice(1);
  }
</script>

<input type="text" bind:value />
<button on:click="{addPerson}">Add person</button>
<button on:click="{removeFirstPerson}">Remove first person</button>

{#each persons as { name, id }, index (id)}
  <Person {name} {index} />
{:else}
  <p>No persons</p>
{/each}
