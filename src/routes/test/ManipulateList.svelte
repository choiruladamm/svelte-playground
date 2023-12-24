<script>
	let items = ['Item 1', 'Item 2', 'Item 3'];
	let newItem = '';

	function addItem() {
		if (newItem.trim() !== '') {
			items = [...items, newItem];
			newItem = '';
		}
	}

	function removeItem(index) {
		items = items.filter((_, i) => i !== index);
	}
</script>

<div class="flex">
	<input type="text" bind:value={newItem} placeholder="type items here..." />
	<button on:click={addItem} disabled={!newItem}>add item</button>
</div>

<ul>
	{#each items as item, index (item + index)}
		<li key={item + index}>{item} <button on:click={() => removeItem(index)}>remove item</button></li>
	{/each}
</ul>

<style>
</style>
