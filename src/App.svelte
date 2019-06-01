<script>
	export let name = 'world';

	import Child from './Child.svelte';

	let data = {
		userId: 123456,
		name: 'John Doe',
		email: 'john@email.com' 
	}
</script>

<style>
	h1{
		color: #6518a9;
		font-family: monospace;
	}
</style>

<h1>Hello, {name}!</h1>

<hr>

<Child {...data} />