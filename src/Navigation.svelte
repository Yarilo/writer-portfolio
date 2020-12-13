<script>
	export let onClickSection;
	export let location;

	const getClass = (linkName, location) => {
		if (linkName === location) return 'selected';
		return ''
	}
</script>

<ul class='navigation-drawer'>
    <li on:click={() => onClickSection("")}><a href="">SV</a></li>
    <li class={getClass('about', location)} on:click={() => onClickSection("about")}><a href="#about">About</a></li>
    <li class={getClass('portfolio', location)} on:click={() => onClickSection("portfolio")}><a href="#portfolio">Portfolio</a></li>
    <li class={getClass('contact', location)} on:click={() => onClickSection("contact")}><a href="#contact">Contact</a></li>
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
</style>