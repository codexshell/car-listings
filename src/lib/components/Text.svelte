<script>
	export let label = 'Label';
	export let variant = '';
</script>

{#if variant === 'h1'}
	<h1>{label}</h1>
{:else if variant === 'h2'}
	<h2>{label}</h2>
{:else if variant === 'p'}
	<p>{label}</p>
{:else if variant === 'price'}
	<span class="price">${label}</span>
{/if}

<style>
	h1 {
		font-weight: 400;
		font-size: 3.2rem;
		line-height: 4rem;
	}

	h2 {
		font-weight: 400;
		font-size: 2.2rem;
		line-height: 2.75rem;
		color: #008ad8;
	}

	p {
		font-weight: 400;
		font-size: 1.8rem;
		line-height: 2.25rem;
		color: #686868;
	}

	.price {
		font-weight: 400;
		font-size: 2.4rem;
		line-height: 3rem;
	}
</style>
