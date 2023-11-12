<script>

</script>

<svelte:head>
	<title>Question 2</title>
	<meta name="description" content="Développement durable - question 2" />
</svelte:head>

<section>
    <div class="question">
		<div class="left">
			<h2>Question 2 :</h2>
		</div>
		<div class="right">
			<p>
                Je vais utiliser des outils d’analyse quelque Lighthouse et GreenIT pour vérifier que ce que je développe est performant, respecte les normes d’accessibilité et est responsable de l’environnement.<br/>
                Ainsi, je vais optimiser les différents développements que j’effectue. Pour cela, j’optimiserais mon code, limiterais les requêtes superflues et aussi effectuer un travail sur les images. Pour les images, il faudra passer par une compression, un bon format (webp) et ne pas les redimensionner dans le code.<br/>
                Je penserais aussi à faire une conception réactive et mobile friendly. Lorsque que j’ai des animations à réaliser je préfèrerais utiliser du CSS plutôt que Javascript pour réduire la charge GPU.<br/>
                J’essaierai aussi de limiter l’utilisation de services tiers pour limiter les requêtes gourmandes.<br/>
                Pour finir, avec les connaissances que j’ai acquises, j’essaierais d’informer les équipes et les clients avec lesquels je travaille.
            </p>
		</div>
	</div>
</section>

<style>
    section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	.question {
		display: flex;
		width: 100%;
	}

	h2 {
		font-size: 1.5rem;
	}

	.left {
		flex: 0.3;
	}

	.right{
		flex: 1;
	}

	@media (max-width: 480px) {
		.question {
			flex-direction: column;
		}
	}
</style>