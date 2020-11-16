<script>
  import People from './people.svelte';

  const peoples = [
    { name: 'Максим', age: 20, job: 'Frontend' },
    { name: 'Елена', age: 20, job: 'Design' },
  ];

  const name = 'Игорь';
  const age = 20;
  const jobTitle = 'Backend';
</script>

<People />

<People
  name="{peoples[0].name}"
  age="{peoples[0].age}"
  job="{peoples[0].job}"
/>

<People {...peoples[1]} />

<People {name} {age} job="{jobTitle}" />
