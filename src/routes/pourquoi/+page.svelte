<script>
    import lighthouse from '$lib/assets/lighthouse.webp'
    import ecoindex from '$lib/assets/ecoindex.webp'
</script>

<svelte:head>
	<title>Pourquoi ?</title>
	<meta name="description" content="Développement durable - Pourquoi ?" />
</svelte:head>

<section>
    <div class="question">
		<div class="left">
			<h2>Pourquoi ?</h2>
		</div>
		<div class="right">
            <div>
                <p>
                    Ce site est conçu et développé de manière responsable. Une score de 100/100 à toutes les étapes de Lighthouse.
                </p>
                <img src={lighthouse} alt="lighthouse" width="300" height="49"/>
                <p>
                    Et une score EcoIndex A.
                </p>
                <img src={ecoindex} alt="ecoindex score" width="400" height="84"/>
            </div>
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

        img {
            max-width: 100%;
        }
	}
</style>