<script>
  export let name = 'Undefined name';
  export let age = 'Undefined age';
  export let job = 'Undefined job';
</script>

<style>
  table {
    border: 1px solid currentColor;
  }
</style>

<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Job</th>
  </tr>
  <tr>
    <td>{name}</td>
    <td>{age}</td>
    <td>{job}</td>
  </tr>
</table>
