<script>
    export let onClickSection;
</script>

<ul class='navigation-drawer'>
    <li on:click={() => onClickSection("")}><a href="">SV</a></li>
    <li on:click={() => onClickSection("about")}><a href="#about">About</a></li>
    <li on:click={() => onClickSection("portfolio")}><a href="#portfolio">Porfolio</a></li>
    <li on:click={() => onClickSection("contact")}><a href="#contact">Contact</a></li>
</ul>
	

<style>
	ul {
		list-style: none;
	}
	li {
		margin-top: 50px;
	}
	a {
		color: black;
	}
	.navigation-drawer {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
</style>