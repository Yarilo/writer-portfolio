<script>
	export let onClickSection;
	export let location;

	const getClass = (linkName, location) => {
		if (linkName === location) return 'selected';
		return ''
	}
</script>

<ul class='navigation-drawer'>
    <li on:click={() => onClickSection("")}><a href="/">SV</a></li>
    <li class={getClass('about', location)} on:click={() => onClickSection("about")}><a href="#about">Sobre mi</a></li>
    <li class={getClass('portfolio', location)} on:click={() => onClickSection("portfolio")}><a href="#portfolio">Portfolio</a></li>
    <li class={getClass('contact', location)} on:click={() => onClickSection("contact")}><a href="#contact">Contacto</a></li>
</ul>
	

<style>
	ul {
		list-style: none;
	}
	li {
		margin-top: 50px;
	}
	
	li.selected {
		text-decoration: underline;
	}

	.navigation-drawer {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	@media (max-width:800px)  { 

		.navigation-drawer{
			height: initial;
			margin-top: 0px;
			display: flex;
			flex-direction: row;
			width: 100%;
			justify-content: space-around;
			padding:0;
		}
	}

</style>