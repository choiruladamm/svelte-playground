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

	function sayDosen() {
		dispatch('myDosenName', {
			message: 'Saya sudah mengumpulkan tugas saya'
		})
	}
</script>

<div>
	<button class="button-50" style="background: darkolivegreen; color: white;" on:click={sayDosen}>
		Click to say hello dispatch
	</button>
</div>
