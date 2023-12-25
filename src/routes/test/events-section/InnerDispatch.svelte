<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function sayHello() {
		dispatch('message', {
			text: 'Hello dispatch svelte'
		});
	}

	function sayAdam() {
		dispatch('adam', {
			axel: 'This my nick name (Black Scythe)'
		});
	}
</script>

<div>
	<button class="button-50" style="background: darkolivegreen; color: white;" on:click={sayAdam}>
		Click to say hello dispatch
	</button>
</div>
