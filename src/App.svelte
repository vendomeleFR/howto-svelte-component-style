<script>
	import Dummy from './Dummy.svelte';
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		font-size: 4em;
		font-weight: 100;
	}

	:global([dummyStyle='ex1']) {
		margin: 10px auto;
		width: 300px;
		height: 200px;
		border: thin solid;
		background: #40a563;
	}

	:global([dummyStyle='ex2']) {
		margin: 0 auto;
		width: 300px;
		height: 200px;
		border: 5px solid;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Svelte Component Style</h1>
	<Dummy dummyStyle="ex1" />
	<Dummy dummyStyle="ex2" />
</main>
