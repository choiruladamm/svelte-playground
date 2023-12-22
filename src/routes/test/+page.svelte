<script>
	import Paragraph from './Paragraph.svelte';

	let name = 'test page about';
	let src = 'https://i.gifer.com/XcF7.gif';
	let gif = 'https://i.gifer.com/hdt.gif';

	let string = `this string contains some <strong>HTML!!!</strong>`;

	let count = 0;
	$: doubled = count * 2

	function increment() {
		count++;
		console.log(`DOM changes ${count}`);
	}
</script>

<div>
	<h1 class="h1">{name.toUpperCase()}</h1>

	<Paragraph />

	<h2>Gif Meme hahahahahaha</h2>
	<div class="flex">
		<img {src} height="300" alt="kodok" />
		<img src={gif} height="300" alt="kodok" />
	</div>

	{@html string}

	<br />

	<button on:click={increment}>
		Count {count}
		{count === 1 ? 'time' : 'times'}
	</button>

	<p>{count} doubled is {doubled}</p>
</div>

<style>
	.h1 {
		font-weight: 600;
	}

	h2 {
		text-align: center;
		font-weight: 700;
		font-size: 2rem;
	}

	.flex {
		margin: 2rem 0;
		text-align: center;
	}

	button {
		margin: 1rem 0;
		padding: 10px 22px;
		border: 0;
		background: darkorange;
		border-radius: 10px;
		cursor: pointer;
		font-weight: 600;
	}
</style>
