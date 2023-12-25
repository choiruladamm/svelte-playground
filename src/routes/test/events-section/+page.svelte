<script>
	import DomEvents from './DomEvents.svelte';
</script>

<svelte:head>
	<title>DOM Events - Test Explore Svelte</title>
	<meta name="description" content="How to using svelte from basic" />
</svelte:head>

<main class="flex">
	<h1>DOM Events - Test Explore Svelte</h1>
	
	<DomEvents />
</main>

<style>
	h1 {
		font-weight: bolder;
	}

	.flex {
		display: flex;
		flex-direction: column;
		gap: 15px;
	}
</style>
