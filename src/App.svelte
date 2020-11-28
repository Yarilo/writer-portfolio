<script>
	import Navigation from './Navigation.svelte';
	import About from "./About.svelte";
	import Title from './Title.svelte';
	import Portfolio from './Portfolio.svelte';
	import Contact from './Contact.svelte'

	let location = window.location.href.split('#')[1]
	const onClickSection = (section) => {
		location = section;
	}
</script>

<main>
	<Navigation onClickSection={onClickSection} />
	<div class='content'>
		<!-- We could simplify this using an array of section, but not needed for now-->
		{#if !location}
			<Title />
		{:else if location === 'about'}
			<About/>
		{:else if location.includes('portfolio')} <!-- TODO Use regexp like /portfolio/:dsdsa-->
			<Portfolio/>
		{:else if location === 'contact'}
			<Contact/>
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
	main :global(a) {
		color: black;
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