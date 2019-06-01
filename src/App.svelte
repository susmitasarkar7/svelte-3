<script>
	export let name = 'world';

	function delay(ms) {
		return new Promise(resolve => setTimeout(resolve));
	}

	let rando = delay(2000).then(v => Math.random());
</script>

<h1>Hello {name}!</h1>

<hr>

{#await rando}
	<p>thinking about it...</p>
{:then number}
	<p>Result {number}</p>
{:catch error}
	<p>{error.message}</p>
{/await}