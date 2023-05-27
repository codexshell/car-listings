<script>
	export let headers = [];
</script>

<div class="table-header">
	{#each headers as header}
		<div class="header">{header}</div>
	{/each}
</div>

<style>
	.table-header {
		height: 5.5rem;
		background-color: #008ad8;
		display: flex;
		justify-content: space-between;
		border-radius: 0.6rem;
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
