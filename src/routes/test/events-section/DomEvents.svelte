<script>
	let m = { x: 0, y: 0 };

	function handleMove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}
</script>

<div
	on:pointermove={(e) => {
		m.x = e.clientX;
		m.y = e.clientY;
	}}
>
	The pointer is at {m.x} x {m.y}
</div>

<style>
	div {
		top: 150px;
		left: 0;
		position: fixed;
		width: 100%;
		height: 100%;
		text-align: center;
	}
</style>
