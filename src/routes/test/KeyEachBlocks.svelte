<script>
	import Emoji from './Emoji.svelte';

	let things = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' }
	];

	function handleDeleteClick() {
		things = things.slice(1);
	}
</script>

<div>
	<button on:click={handleDeleteClick}>Remove first thing</button>
	<ul>
		{#each things as thing (thing.id)}
			<Emoji name={thing.name} />
		{/each}
	</ul>
</div>
