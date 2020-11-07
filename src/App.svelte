<script>
	
</script>

<main>
	<ul class='navigation-drawer'>
		<li>About</li>
		<li>Portfolio</li>
		<li>Contact</li>
	</ul>
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

	.title {
		text-align: center;
		flex: 2;
	}
	h1 {
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