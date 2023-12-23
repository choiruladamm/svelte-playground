<script>
	export let name;
	export let speed;
	export let version;
	export let website;

	$: href = `https://www.npmjs.com/package/${name}`;
</script>

<p>
	The <code>{name}</code> package is {speed} fast. Download version {version} from <a {href}>npm</a>
	and <a href={website}>learn more here</a>
</p>

<style>
	code {
		font-size: 16px;
		font-weight: 600;
		font-family: 'Courier New', Courier, monospace;
		background-color: white;
		border-radius: 3px;
		padding: 0.5rem;
	}
</style>
