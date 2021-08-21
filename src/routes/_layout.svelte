<script>
	import '../styles/theme.css';
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<Nav {segment} />

<main>
	<slot />
</main>

<style>
	:global(#sapper) {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		font-family: 'Montserrat', sans-serif;
	}

	:global(ul) {
		padding-left: 1.5em;
	}

	:global(p) {
		line-height: 1.5;
	}
</style>
