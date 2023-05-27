<slot />

<style>
	@import url('https://fonts.googleapis.com/css2?family=Lexend+Deca:wght@100;200;300;400;500;600;700;800;900&display=swap');
	@import '../../node_modules/@csstools/normalize.css/normalize.css';

	:global(:root) {
		font-size: 62.5%;
	}

	:global(body) {
		font-size: 1.6rem;
		box-sizing: border-box;
	}

	:global(*, *::before, *::after) {
		box-sizing: inherit;
		margin: 0;
		padding: 0;
		font-family: 'Lexend Deca', sans-serif;
	}
</style>
