<script>
	import { fly } from 'svelte/transition';

	import search from '$lib/images/search.svg';
	import threeDots from '$lib/images/three-dots.svg';

	export let filterOptions = [];

	let showModal = false;
	const toggleModal = () => {
		showModal = !showModal;
	};
</script>

<div class="container">
	<div class="input-wrapper">
		<input type="text" /> <button class="search-btn"><img src={search} alt="" /></button>
	</div>
	<button on:click={toggleModal} class="menu-btn">
		<img src={threeDots} alt="menu" />
	</button>

	{#if showModal}
		<div
			transition:fly={{
				y: 100,
				duration: 250
			}}
			class="modal"
		>
			{#each filterOptions as option}
				<div class="option-wrapper">
					<input id={option} type="checkbox" />
					<label for={option}>
						{option}
					</label>
				</div>
			{/each}
		</div>
	{/if}
</div>

<style>
	.container {
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 1.5rem;
		position: relative;
	}

	.input-wrapper {
		position: relative;
	}

	button {
		border: none;
		background: transparent;
		cursor: pointer;
	}

	input {
		width: 27.8rem;
		height: 3.9rem;
		background-color: white;
		border: none;
		border-radius: 3.6rem;
		padding-inline: 1.6rem;
		padding-right: 5rem;
	}

	.search-btn {
		position: absolute;
		right: 0;
		top: 0;
		height: 100%;
		width: 4.8rem;
		border-radius: 0 3.6rem 3.6rem 0;
		transition: all 0.25s ease-in-out;
	}

	.search-btn:hover {
		background-color: #008ad8;
	}

	.modal {
		width: 25.7rem;
		min-height: 20.6rem;
		background-color: white;
		position: absolute;
		top: 0;
		right: 0;
		margin-top: 5rem;
		margin-right: 5rem;
		box-shadow: 1.1rem 1.8rem 5.4rem rgba(0, 0, 0, 0.11);
		border-radius: 0.6rem;
		padding: 3rem;
	}

	.option-wrapper {
		display: flex;
		gap: 2rem;
		align-items: center;
		margin-bottom: 1.8rem;
	}

	.option-wrapper:last-child {
		margin-bottom: 0;
	}

	input[type='checkbox'] {
		width: fit-content;
		height: fit-content;
	}

	label {
		font-size: 1.8rem;
	}
</style>
