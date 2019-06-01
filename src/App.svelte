<script>
	export let name = 'world';

	import Child from './Child.svelte';

	let data = {
		userId: 123456,
		name: 'John Doe',
		email: 'john@email.com' 
	}
</script>

<h1>Hello {name}!</h1>

<hr>

<Child {...data} />