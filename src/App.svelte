<script>
	import { fade, fly } from 'svelte/transition';

	export let name = 'world';

	let randos = [];

	function setrando() {
		const rando = Math.random(Math.random() * 100);
		randos = [...randos, rando]
	}
</script>

<h1>Hello {name}!</h1>

<hr>

<button on:click={setrando}>Push</button>
