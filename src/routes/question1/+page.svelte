<script>

</script>

<svelte:head>
	<title>Question 1</title>
	<meta name="description" content="Développement durable - question 1" />
</svelte:head>

<section>
    <div class="question">
		<div class="left">
			<h2>Question 1 :</h2>
		</div>
		<div class="right">
			<ul>
				<li>
					En tant que responsable de la sécurité, je veux que la solution SaaS intègre directement des mécanismes avancés de sécurité comme une authentification multifactorielle, une surveillance en temps réel des menaces ou des sauvegardes pour garantir l’intégrité des données.
				</li>
				<li>
					En tant que directeur des opérations, il est important que la solution soit transparente sur sa sobriété numérique en proposant par exemple des rapports de suivi afin de connaître la consommation énergétique et de bande passante ou encore son empreinte carbone.
				</li>
				<li>
					En tant que personne chargé de la conformité, je m’assure que cette solution respecte la protection des données (RGPD) et propose un stockage sécurisé des données personnelles.
				</li>
				<li>
					En tant que directeur financier, je veux que la tarification soit basée sur l’utilisation réelle des ressources ainsi elle est transparente. Cela permettra d’optimiser les coûts et d’éviter le gaspillage.
				</li>
				<li>
					En tant que responsable accessibilité, il faut que la solution soit accessible aux personnes en situation de handicape afin de favoriser l’inclusion numérique.
				</li>
				<li>
					En tant que responsable performance, je souhaite que la solution optimise la gestion des requêtes et les transferts de connées afin de réduire la consommation énergétique.
				</li>
				<li>
					En tant qu’administrateur système et réseau, je veux que la solution Saas est une disponibilité de 99,9 % pour une bonne continuité de service.
				</li>
				<li>
					En tant que responsable des achats, je choisis un fournisseur qui s’engage à réduire son empreinte carbone.
				</li>
				<li>
					En tant que responsable environnement, je m’assure que la solution favorise l’efficacité énergétique que minimisant la consommation des ressources informatiques.
				</li>
			</ul>
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
		transition: all linear .2s;
	}

	ul li:hover {
		scale: 1.2;
	}

	ul li::before {
		content: "-";
		position: absolute;
		left: -1rem;
	}
</style>