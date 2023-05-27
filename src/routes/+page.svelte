<script>
	// import Text from '$lib/components/Text.svelte';
	// import SearchInput from '$lib/components/SearchInput.svelte';
	// import CarEntry from '$lib/components/CarEntry.svelte';
	import TableHeader from '$lib/components/TableHeader.svelte';

	// const filterOptions = ['New cars', 'Used cars', 'Dealership', 'For sale by owner'];
	const tableHeaders = ['Car details', 'Location', 'Price', 'Action'];
</script>

<main>
	<TableHeader headers={tableHeaders} />
</main>

<style>
	main {
		background-color: papayawhip;
		height: 100vh;
	}
</style>
