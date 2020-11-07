<script>
	import Navigation from './Navigation.svelte';
	import About from "./About.svelte";
</script>

<main>
	<Navigation />
	<div class='title'>
		<h1>SV</h1>
		<h2>Screenwriter</h2>
	</div>
	
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Courier+Prime&display=swap');
	main {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
		font-family: 'Courier Prime', monospace;
	}

	.title {
		text-align: center;
		flex: 2;
	}

	h1 {
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	
</style>