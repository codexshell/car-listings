<script>
	export let headers = [];
</script>

<div class="table-header" style="--cols: {headers.length}">
	{#each headers as header}
		<div class="header">{header}</div>
	{/each}
</div>

<style>
	.table-header {
		height: 5.5rem;
		background-color: #008ad8;
		display: grid;
		grid-template-columns: repeat(var(--cols), 1fr);
	}

	.header {
		color: white;
		text-transform: uppercase;
		font-weight: 400;
		font-size: 1.4rem;
		line-height: 1.75rem;
		padding: 2rem;
	}
</style>
