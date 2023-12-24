<script>
	const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];
	let selected = colors[0];
</script>

<div class="content" style="background: {selected};">hahahahahahahah</div>

<div class="flex">
	{#each colors as color, i}
		<button
			class="button-50"
			style="background: {color};"
			aria-label={selected}
			aria-current={selected === color}
			on:click={() => (selected = color)}>{i + 1}</button
		>
	{/each}
</div>

<style>
	.content {
		margin: 1rem 0;
		background-color: red;
		padding: 20px;
		text-align: center;
		color: white;
	}

	.flex {
		display: flex;
		gap: 10px;
		justify-content: center;
		flex-direction: column;
	}

	.button-50 {
		appearance: button;
		background-color: #000;
		background-image: none;
		border: 1px solid #000;
		border-radius: 4px;
		box-shadow:
			#fff 4px 4px 0 0,
			#000 4px 4px 0 1px;
		box-sizing: border-box;
		color: #fff;
		cursor: pointer;
		display: inline-block;
		font-family: ITCAvantGardeStd-Bk, Arial, sans-serif;
		font-size: 14px;
		font-weight: 400;
		line-height: 20px;
		margin: 0 5px 10px 0;
		overflow: visible;
		padding: 12px 40px;
		text-align: center;
		text-transform: none;
		touch-action: manipulation;
		user-select: none;
		-webkit-user-select: none;
		vertical-align: middle;
		white-space: nowrap;
	}

	.button-50:focus {
		text-decoration: none;
	}

	.button-50:hover {
		text-decoration: none;
	}

	.button-50:active {
		box-shadow: rgba(0, 0, 0, 0.125) 0 3px 5px inset;
		outline: 0;
	}

	.button-50:not([disabled]):active {
		box-shadow:
			#fff 2px 2px 0 0,
			#000 2px 2px 0 1px;
		transform: translate(2px, 2px);
	}

	@media (min-width: 1024px) {
		.button-50 {
			padding: 12px 50px;
		}

		.flex {
			display: flex;
			flex-direction: row;
		}
	}
</style>
