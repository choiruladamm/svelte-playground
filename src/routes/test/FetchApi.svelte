<script>
	import { onMount } from 'svelte';

	let data = [];

	async function fetchData() {
		try {
			const res = await fetch('https://jsonplaceholder.typicode.com/todos');
			const result = await res.json();
			data = result.slice(0,10)
      console.log(data);
		} catch (error) {
			console.log('Error fetching data: ', error);
		}
	}

	onMount(fetchData);
</script>

<ul>
  {#each data as todo (todo.id)}
     <li>{todo.title}</li>
  {/each}
</ul>
