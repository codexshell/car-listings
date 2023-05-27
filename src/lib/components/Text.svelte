<script>
	export let label = 'Label';
	export let variant = '';
	export let top = 0;

	let topRem = `${top / 10}rem`;
</script>

{#if variant === 'h1'}
	<h1 style="--top: {topRem}">{label}</h1>
{:else if variant === 'h2'}
	<h2 style="--top: {topRem}">{label}</h2>
{:else if variant === 'p'}
	<p style="--top: {topRem}">{label}</p>
{:else if variant === 'price'}
	<span style="--top: {topRem}" class="price">{label}</span>
{/if}

<style>
	h1 {
		font-weight: 400;
		font-size: 3.2rem;
		line-height: 4rem;
		margin-top: var(--top);
	}

	h2 {
		font-weight: 400;
		font-size: 2.2rem;
		line-height: 2.75rem;
		color: #008ad8;
		margin-top: var(--top);
	}

	p {
		font-weight: 400;
		font-size: 1.8rem;
		line-height: 2.25rem;
		color: #686868;
		margin-top: var(--top);
	}

	.price {
		font-weight: 400;
		font-size: 2.4rem;
		line-height: 3rem;
		margin-top: var(--top);
	}
</style>
