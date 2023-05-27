<script>
	import Text from '$lib/components/Text.svelte';
	import SearchInput from '$lib/components/SearchInput.svelte';
	import CarEntry from '$lib/components/CarEntry.svelte';
	import TableHeader from '$lib/components/TableHeader.svelte';

	const filterOptions = ['New cars', 'Used cars', 'Dealership', 'For sale by owner'];
	const tableHeaders = ['Car details', 'Location', 'Price', 'Action'];
	const carCollection = [
		{
			name: '2017 Toyota Highlander V4',
			street: '1944 Scrimba Ln',
			city: 'Youngstown',
			state: 'OH',
			zip: '4481',
			price: '17400'
		},
		{
			name: '2012 Toyota Tundra 4x4',
			street: '301 Fantasy Dr',
			city: 'Beverly Hills',
			state: 'CA',
			zip: '90210',
			price: '23900'
		},
		{
			name: '2004 Dodge Ram 4x4',
			street: '9104 Falsety Ave',
			city: 'AnonyVille',
			state: 'FL',
			zip: '40440',
			price: '7988'
		},
		{
			name: '2021 Tesla Model 3',
			street: '993 Fiscal St',
			city: 'Boulder',
			state: 'CO',
			zip: '9391',
			price: '37490'
		},
		{
			name: '2017 Toyota Highlander V4',
			street: '1944 Scrimba Ln',
			city: 'Youngstown',
			state: 'OH',
			zip: '44481',
			price: '17400'
		},
		{
			name: '2012 Toyota Tundra 4x4',
			street: '301 Fantasy Dr',
			city: 'Beverly Hills',
			state: 'CA',
			zip: '90210'
		}
	];
</script>

<main>
	<div class="wrapper">
		<Text label="Available Cars" variant="h1" />
		<Text top="7" label="There are 15 cars that match your criteria" variant="p" />
		<div class="search-wrapper">
			<SearchInput top="26" {filterOptions} />
		</div>

		<div class="table-header-wrapper">
			<TableHeader headers={tableHeaders} />
		</div>
		<div class="collection-wrapper">
			{#each carCollection as car}
				<CarEntry
					name={car.name}
					street={car.street}
					city={car.city}
					state={car.state}
					zip={car.zip}
					price={car.price}
				/>
			{/each}
		</div>
	</div>
</main>

<style>
	main {
		background-color: #e5e5e5;
		min-height: 100vh;
		padding: 4.1rem 2.6rem;
	}

	.collection-wrapper {
		margin-top: 6.8rem;
	}

	.wrapper {
		max-width: 1440px;
		margin: 0 auto;
	}

	.table-header-wrapper {
		display: none;
	}

	@media only screen and (min-width: 1280px) {
		main {
			padding: 9.2rem 10rem;
		}

		.collection-wrapper {
			margin: 0;
		}

		.table-header-wrapper {
			display: block;
			margin-top: 5.1rem;
		}

		.search-wrapper {
			display: flex;
			justify-content: right;
		}
	}
</style>
