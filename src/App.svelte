<script>
	export let name = 'world';

	import { randomStore } from './store';
</script>

<h1>Hello {name}!</h1>

<hr>

	{$randomStore}

<hr>

<button on:click={() => randomStore.set(Math.random()}>
</button>