<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	main {
		max-width: 56em;
		padding: 2em;
		margin: 2em;

		border: 2px solid var(--main-fg-color);
		background-color: var(--main-bg-color);
	}
</style>

<main>
	<Nav {segment}/>
	<slot></slot>
</main>