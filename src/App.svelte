<script>
	export let name = 'world';

	let rando;

	$: result = Math.round(rando) ? 'winner' : 'looser' ;

	function setrando() {
		rando = Math.random();
	}
</script>

<h1>Hello {name}!</h1>

<p>The random number is {rando}</p>

<hr>

<p>{result}</p>
<p>{result}</p>
<p>{result}</p>

<button on:click={setrando}>Randomize</button>

<input bind:value={rando}>