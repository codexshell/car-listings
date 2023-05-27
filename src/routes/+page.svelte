<script>
	// import Text from '$lib/components/Text.svelte';
	// import SearchInput from '$lib/components/SearchInput.svelte';
	import CarEntry from '$lib/components/CarEntry.svelte';

	// const filterOptions = ['New cars', 'Used cars', 'Dealership', 'For sale by owner'];
</script>

<main>
	<CarEntry name="Car name" location="Car location" price="17400" />
</main>

<style>
	main {
		background-color: papayawhip;
		height: 100vh;
	}
</style>
