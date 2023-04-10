<script>
	// @ts-nocheck

	import '@picocss/pico';
	import '../app.css';

	import burger from '$lib/assets/icons/burger.svg';
	import logo from '$lib/assets/logo_nobg_sm.webp';
	import { page } from '$app/stores';

	let isBurgerOpen = false;
	let oldYPos = 0;
	let y = 0;

	/**
	 * @param {any} node
	 */
	function clickOutside(node) {
		const handleClick = (/** @type {any} **/ event) => {
			if (
				!node.contains(event.target) &&
				!document.getElementById('burger-button')?.contains(event.target)
			) {
				node.dispatchEvent(new CustomEvent('outclick'));
			}
		};

		document.addEventListener('click', handleClick, true);

		return {
			destroy() {
				document.removeEventListener('click', handleClick, true);
			}
		};
	}

	function toggleBurgerNav() {
		isBurgerOpen = !isBurgerOpen;
	}

	function shouldShowHeader(actualYPos) {
		if (actualYPos <= 100) {
			return true;
		}

		if (actualYPos < oldYPos) {
			oldYPos = actualYPos;
			return true;
		}

		oldYPos = actualYPos;
		return false;
	}
</script>

<svelte:window bind:scrollY={y} />

<header class:hidden={!shouldShowHeader(y)}>
	<nav class="container">
		<ul>
			<li>
				{#if $page.url.pathname === '/'}
					<a class="contrast" href="#">
						<img src={logo} alt="Main Page" id="page-logo" />
					</a>
				{:else}
					<a class="contrast" href="/">
						<img src={logo} alt="Main Page" id="page-logo" />
					</a>
				{/if}
			</li>
		</ul>

		<div
			id="burger-button"
			class="burger-button nav-area secondary"
			role="button"
			aria-roledescription="Opens the navigation"
			on:click={toggleBurgerNav}
			on:keydown={toggleBurgerNav}
			tabindex="0"
		>
			<img src={burger} alt="Burger Button" />
		</div>

		<ul
			class="nav-links nav-area"
			use:clickOutside
			on:outclick={() => (isBurgerOpen = false)}
			class:active={isBurgerOpen}
		>
			<li><a class="nav-link" href="/about">Sobre Nós</a></li>
			<li><a class="nav-link" href="/roda-de-cura">Roda de Cura</a></li>
			<li><a class="nav-link" href="/dalet">Dalet</a></li>
		</ul>
	</nav>
</header>

<slot />

<footer>
	<div class="container">
		<div class="brand">Servos de Luz</div>
		<div class="copyright">
			© {new Date().getFullYear()} Servos de Luz. Todos os direitos reservados.
		</div>
		<nav class="links">
			<ul>
				<li><a class="nav-link" href="/about">Sobre Nós</a></li>
				<li><a class="nav-link" href="/roda-de-cura">Roda de Cura</a></li>
				<li><a class="nav-link" href="/dalet">Dalet</a></li>
			</ul>
		</nav>
	</div>
</footer>

<style>
	header {
		z-index: 15;
		background-color: var(--secondary);
		color: var(--primary-inverse);
		position: fixed;
		top: 0;
		width: 100%;

		transition: 250ms;
	}

	header.hidden {
		transform: translateY(-100%);
	}

	header * {
		color: var(--primary-inverse);
	}

	#page-logo {
		cursor: pointer;
		border-radius: 15px;
		width: 72px;
		transition: transform 425ms;
	}

	#page-logo:hover,
	.nav-link:hover {
		transform: translateY(-2%);
		transition: transform 425ms;
	}

	.nav-link {
		display: block;
		transition: transform 425ms;
	}

	.burger-button {
		display: none;
	}

	@media (max-width: 900px) {
		.nav-links {
			display: none;
		}

		.nav-links.active {
			background-color: var(--secondary);
			display: flex;
			flex-direction: column;
			position: fixed;
			top: 10%;
			right: 3.6%;
			padding: 0 30px 0 25px;
			border-radius: var(--border-radius);
		}

		.burger-button {
			display: flex;
			margin: auto 0;
		}
	}

	footer {
		background-color: var(--secondary);
	}

	footer * {
		color: var(--primary-inverse);
	}

	footer .container {
		padding: 5rem 10rem 1rem 10rem;
		margin: 0 auto;
		max-width: 1560px;
		display: flex;
		justify-content: space-between;
		align-items: baseline;
	}

	footer .brand {
		font-size: 2rem;
	}

	footer .copyright {
		font-size: 1rem;
	}

	footer .links ul {
		display: flex;
		flex-direction: column;
		align-items: baseline;
		list-style: none;
	}

	@media (max-width: 900px) {
		footer .container {
			flex-direction: column;
			padding: 2rem 2rem 1rem 2rem;
		}
	}
</style>
