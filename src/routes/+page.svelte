<script>
	// import Text from '$lib/components/Text.svelte';
	import SearchInput from '$lib/components/SearchInput.svelte';

	const filterOptions = ['New cars', 'Used cars', 'Dealership', 'For sale by owner'];
</script>

<main>
	<SearchInput {filterOptions} />
</main>

<style>
	main {
		display: grid;
		place-content: center;
		background-color: papayawhip;
		height: 100vh;
	}
</style>
