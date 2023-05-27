<script>
	import Text from '$lib/components/Text.svelte';

	import heartFilled from '$lib/images/heart-filled.svg';
	import heartStroke from '$lib/images/heart-stroke.svg';

	export let name = 'Car name';
	export let street = 'Street';
	export let city = 'City';
	export let state = 'State';
	export let zip = '00000';
	export let price = 'Car price';

	let isFavorite = false;
	const formattedPrice = new Intl.NumberFormat('en-US', {
		style: 'currency',
		currency: 'USD',
		maximumFractionDigits: 0
	}).format(price);

	function toggleFavorite() {
		isFavorite = !isFavorite;
	}
</script>

<div class="container">
	<Text label={name} variant="h2" />
	<div class="location">
		<Text variant="p" label={street} />
		<div class="city-state">
			<Text variant="p" label={city + ', '} />
			<Text variant="p" label={state} />
			<Text variant="p" label={zip} />
		</div>
	</div>
	<div class="description">
		<Text variant="price" label={formattedPrice} />
		{#if isFavorite}
			<button on:click={toggleFavorite} class="img-wrapper">
				<img src={heartFilled} alt="Favorite" />
			</button>
		{:else}
			<button on:click={toggleFavorite} class="img-wrapper">
				<img src={heartStroke} alt="Not favorite" />
			</button>
		{/if}
	</div>
</div>

<style>
	.container {
		min-width: 38.2rem;
		height: 17.7rem;
		border-radius: 0.6rem;
		padding-top: 1.5rem;
		padding-left: 1.8rem;
		padding-bottom: 1.8rem;
		padding-right: 1.7rem;
		cursor: pointer;
	}

	.container:hover {
		background-color: white;
	}

	.location {
		margin-top: 1.2rem;
	}

	.description {
		margin-top: 2.8rem;
		display: flex;
		justify-content: space-between;
	}

	.img-wrapper {
		background-color: transparent;
		border: none;
		cursor: pointer;
		transition: all 0.2s ease-in-out;
	}

	.img-wrapper:hover {
		transform: scale(1.5);
	}

	.city-state {
		display: flex;
		gap: 0.5rem;
	}

	@media only screen and (min-width: 1280px) {
		.container {
			height: 8.9rem;
			display: grid;
			grid-template-columns: repeat(3, 1fr);
			padding: 2.1rem 4.6rem 1.6rem 2.3rem;
		}

		.location {
			margin: 0;
		}

		.description {
			margin: 0;
		}
	}
</style>
