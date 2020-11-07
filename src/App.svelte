<script>
	
</script>

<main>
	<ul class='navigation-drawer'>
		<li>About</li>
		<li>Portfolio</li>
		<li>Contact</li>
	</ul>
	<h1>SV</h1>
</main>

<style>

	ul {
		list-style: none;
	}
	li {
		margin-top: 50px;
	}
	.navigation-drawer {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	main {
		width:100%;
		height: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	h1 {
		text-align: center;
		flex:2;
		color: black;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>