<script>
	
</script>

<svelte:head>
	<title>Accueil</title>
	<meta name="description" content="Développement durable" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			Bienvenue
		</span>

		sur mon devoir.
	</h1>

	<h2 class="subtitle">
		Bonne visite 😉 !
	</h2>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		font-size: 2rem;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 5rem 0;
		font-size: 4rem;
	}

	.subtitle {
		margin-top: 4rem;
		text-transform: uppercase;
		font-size: 1.2rem;
	}
</style>
