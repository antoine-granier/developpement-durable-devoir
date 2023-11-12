<script>
	import { page } from "$app/stores";
	import leaf from "$lib/assets/leaf.svg";
	import github from "$lib/assets/github.svg";
	import { browser } from "$app/environment";

	let open = false;
</script>

<header>
	<div class="corner">
		{#if browser && window.innerWidth <= 480}
			<div class={open ? "menu-burger active" : "menu-burger"} on:click={() => (open = !open)}>
				<span />
				<span />
			</div>
		{:else}
			<img src={leaf} alt="Logo" />
		{/if}
	</div>

	{#if browser && window.innerWidth > 480}
		<nav class="navbar">
			<svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
			</svg>
			<ul>
				<li
					aria-current={$page.url.pathname === "/"
						? "page"
						: undefined}
				>
					<a href="/">Accueil</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question1"
						? "page"
						: undefined}
				>
					<a href="/question1">Question 1</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question2"
						? "page"
						: undefined}
				>
					<a href="/question2">Question 2</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question3"
						? "page"
						: undefined}
				>
					<a href="/question3">Question 3</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question4"
						? "page"
						: undefined}
				>
					<a href="/question4">Question 4</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/pourquoi"
						? "page"
						: undefined}
				>
					<a href="/pourquoi">Pourquoi ?</a>
				</li>
			</ul>
			<svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
			</svg>
		</nav>
	{/if}

	{#if browser && window.innerWidth <= 480}
		<div class={open ? "menu active" : "menu"}>
			<ul>
				<li
					aria-current={$page.url.pathname === "/"
						? "page"
						: undefined}
				>
					<a href="/" on:click={() => (open = false)}>Accueil</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question1"
						? "page"
						: undefined}
				>
					<a href="/question1" on:click={() => (open = false)}>Question 1</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question2"
						? "page"
						: undefined}
				>
					<a href="/question2" on:click={() => (open = false)}>Question 2</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question3"
						? "page"
						: undefined}
				>
					<a href="/question3" on:click={() => (open = false)}>Question 3</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/question4"
						? "page"
						: undefined}
				>
					<a href="/question4" on:click={() => (open = false)}>Question 4</a>
				</li>
				<li
					aria-current={$page.url.pathname === "/pourquoi"
						? "page"
						: undefined}
				>
					<a href="/pourquoi" on:click={() => (open = false)}>Pourquoi ?</a>
				</li>
			</ul>
		</div>
	{/if}

	<div class="corner">
		<a
			href="https://github.com/antoine-granier/developpement-durable-devoir"
			target="_blank"
		>
			<img src={github} alt="GitHub" />
		</a>
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.corner {
		width: 3em;
		height: 3em;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 1rem;
	}

	.corner img {
		width: 2.5em;
		height: 2.5em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2.5em;
		height: 2.5em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	.navbar li[aria-current="page"]::before {
		--size: 6px;
		content: "";
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}

	.menu {
		position: absolute;
		top: 0;
		right: 0;
		width: 100vw;
		height: 0;
		transition: height 0.5s;
		z-index: 90;
		background-color: white;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}

	.menu.active {
		height: 100vh;
		position: fixed;
		top: 0;
		left: 0;
	}

	.menu-burger {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		gap: 4px;
		width: fit-content;
		height: fit-content;
		background-color: transparent;
		cursor: pointer;
		z-index: 99;
	}

	.menu-burger span {
		height: 4px;
		border-radius: 10px;
		background-color: black;
	}

	.menu-burger span:first-child {
		width: 25px;
		transform-origin: 30% -20%;
		transition: transform 0.4s ease-in-out;
	}

	.menu-burger span:last-child {
		width: 12px;
		transform-origin: 20% 100%;
		transition: all 0.4s ease-in-out;
	}

	.menu ul {
		display: none;
		list-style: none;
		padding: 0;
		margin: 0;
		width: 100%;
	}

	.menu ul a {
		text-decoration: none;
		color: black;
		padding: 10px;
		font-size: 2rem;
	}

	.menu ul li[aria-current="page"] a {
		color: var(--color-theme-1);
		text-decoration: underline;
	}

	.menu.active ul {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 30px;
	}

	.menu-burger.active span:first-child {
		transform: rotate(45deg);
	}

	.menu-burger.active span:last-child {
		transform: rotate(-45deg);
		width: 25px;
	}
</style>
