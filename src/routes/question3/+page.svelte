<script>

</script>

<svelte:head>
	<title>Question 3</title>
	<meta name="description" content="Développement durable - question 3" />
</svelte:head>

<section>
    <div class="question">
		<div class="left">
			<h2>Question 3 :</h2>
		</div>
		<div class="right">
            <div>
                <p>Ma société est à taille humaine. En effet nous sommes 19 salariés. Ainsi, elle n’a pas les moyens d’une grande entreprise pour effectuer autant d’actions. Les principales actions effectuées sont :</p>
                <ul>
                    <li>
                        Audit pour l’accessibilité, les performances et la sécurité de ses sites
                    </li>
                    <li>
                        Démarche qualité Qualiopi pour les formations qu’elle propose
                    </li>
                </ul>
                <p>Mais il manque principalement la démarche environnementale. Il y a une utilisation importante d’emails, les employés ne sont pas forcément au courant des impacts important du numérique sur l’écologie. Ainsi c’est sur ce point en particulier qu’il faudrait appuyer. A mon échelle je fais attention car j’ai connaissance de cela. Mais il serait bien de faire une journée avec un webinaire par exemple pour sensibiliser l’ensemble des employés aux bonnes pratiques et aux enjeux qui sont présents.</p>
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

    ul {
		list-style-type: none;
		padding: 0;
	}

	ul li {
		margin-left: 1rem;
		position: relative;
		padding: .3rem 0;
	}

	ul li::before {
		content: "-";
		position: absolute;
		left: -1rem;
	}
</style>