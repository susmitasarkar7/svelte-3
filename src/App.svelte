<script>
	export let name = 'world';

	let rando;

	$: result = Math.round(rando * 100) ;

	function setrando() {
		rando = Math.random();
	}
</script>

<h1>Hello {name}!</h1>

<p>The random number is {rando}</p>

<hr>

<button on:click={setrando}>Randomize</button>

<p>Your score is {result}</p>

{#if result > 75}
	<p>Big winner! top 25%</p>
{:else if result > 50}
	<p>Decent, top 50%</p>
{:else}
	<p>Loser</p>
{/if}