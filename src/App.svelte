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
	<Navigation location={location} onClickSection={onClickSection} />
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

	@media (max-width:800px)  { 
		main{
			display: flex;
			flex-direction: column;
		}
	}

</style>