<script>
	import Answer from './Answer.svelte';
	import Haha from './Haha.svelte';
	import PackageInfo from './PackageInfo.svelte';
	import Paragraph from './Paragraph.svelte';
	import CloneListButton from './CloneListButton.svelte';
	import ManipulateList from './ManipulateList.svelte';
	import KeyEachBlocks from './KeyEachBlocks.svelte';
	import FetchApi from './FetchApi.svelte';
	import ButtonColorList from './ButtonColorList.svelte';
	import { ArrowRight } from 'lucide-svelte';

	let name = 'test page about';
	let src = 'https://i.gifer.com/XcF7.gif';
	let gif = 'https://i.gifer.com/hdt.gif';

	let string = `this string contains some <strong>HTML!!!</strong>`;

	let count = 0;
	$: doubled = count * 2;

	function increment() {
		count++;
		// console.log(`DOM changes ${count}`);
	}

	// $: {
	// 	console.log(`the count is ${count}`);
	// 	console.log(`this will also be logged whenever count changes`);
	// }

	$: if (count >= 10) {
		alert('count is dangerous hight!!!');
		count = 0;
	}

	let numbers = [1, 2, 3, 4];

	function addNumbers() {
		numbers = [...numbers, numbers.length + 1];
	}

	$: sum = numbers.reduce((total, currentNumber) => total + currentNumber, 0);

	let data = 0;

	const pkg = {
		name: 'svelte',
		speed: 'blazing',
		version: 4,
		website: 'https://svelte.dev'
	};
</script>

<svelte:head>
	<title>Test Explore Svelte</title>
	<meta name="description" content="How to using svelte from basic" />
</svelte:head>

<main>
	<h1 class="h1">{name.toUpperCase()}</h1>

	<a style="font-weight: bolder;" href="/test/events-section"
		><div style="display: flex; align-items: center;">
			Go to events section <ArrowRight />
		</div></a
	>

	<Paragraph />

	<h2>Gif Meme hahahahahaha</h2>
	<div class="flex">
		<img {src} height="300" alt="kodok" />
		<img src={gif} height="300" alt="kodok" />
	</div>

	{@html string}

	<button on:click={increment}>
		Count {count}
		{count === 1 ? 'time' : 'times'}
	</button>

	<p>{count} doubled is {doubled}</p>
	<!-- optional -->
	<p>{count} doubled is {count * 2}</p>

	<p><strong> {numbers.join(' + ')} = {sum}</strong></p>

	<button on:click={addNumbers}>Add a number</button>

	<p>{data}</p>
	<div class="btn-group">
		<button on:click={() => (data += 1)}>Increment</button>
		<button on:click={() => (data -= 1)}>Decrement</button>
	</div>

	<p><strong>{numbers.join(' + ')} = {sum}</strong></p>

	<Answer answer={3} />

	<Haha />

	<PackageInfo {...pkg} />

	<button on:click={() => data++}>
		simple counter is count {data}
	</button>

	{#if data > 10}
		<p style="font-weight: bolder;">{data} is greather than 10</p>
	{:else if data < 5}
		<p style="font-weight: bolder;">{data} is less than 5</p>
	{:else}
		<p style="font-weight: bolder;">{data} is between 5 and 10</p>
	{/if}

	<div style="display: flex; flex-direction: column; gap: 15px;">
		<CloneListButton />
		<ButtonColorList />
		<ManipulateList />
		<KeyEachBlocks />
		<FetchApi />
	</div>
</main>

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
