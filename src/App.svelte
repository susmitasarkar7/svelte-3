<script>
	import { fade, fly } from 'svelte/transition;

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
	<p transition:fade>Big winner! top 25%</p>
{:else if result > 50}
	<p>Decent, top 50%</p>
{:else}
	<p
		in:fly={{ x:1000, duration:500 }}
		out:fly={{ x:-500, duration:500 }}
	>Loser</p>
{/if}