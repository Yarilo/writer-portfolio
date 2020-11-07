<script>
	import Navigation from './Navigation.svelte';
	import About from "./About.svelte";
	import Title from './Title.svelte';
</script>

<main>
	<Navigation />
	<Title />
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
	
</style>