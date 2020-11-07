<script>
	import Navigation from './Navigation.svelte';
	import About from "./About.svelte";
	import Title from './Title.svelte';

	let location = window.location.href.split('#')[1]
	const onClickSection = (section) => {
		location = section;
	}
</script>

<main>
	<Navigation onClickSection={onClickSection} />
	<div class='content'>
		{#if !location}
			<Title />
		{:else if location === 'about'}
			<About/>
		{/if}
	</div>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Courier+Prime&display=swap');
	main {
		font-family: 'Courier Prime', monospace;
		width: 100%;
		height: 100%;

		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.content {
		width: 100%;
		height: 100%;

		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
</style>