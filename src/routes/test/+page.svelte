<script>
	let name = 'test page about';
	let src = 'https://i.gifer.com/XcF7.gif';
	let gif = 'https://i.gifer.com/hdt.gif';
</script>

<div>
	<h1 class="h1">{name.toUpperCase()}</h1>

	<p>
		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae id eos ea ducimus commodi
		soluta inventore doloribus in molestiae quae, dolorum aut omnis debitis ipsa nobis suscipit,
		accusantium vitae maiores.
	</p>

	<div class="flex">
		<img {src} height="300" alt="kodok" />
		<img src={gif} height="300" alt="kodok" />
	</div>
</div>

<style>
	.h1 {
		font-weight: 600;
	}

	.flex {
		text-align: center;
	}
</style>
