<script>
	import '@picocss/pico';
	import '../app.css';

	import burger from '$lib/assets/icons/burger.svg';
	import logo from '$lib/assets/logo_nobg_sm.webp';
	import { page } from '$app/stores';

	let open = false;

	/**
	 * @param {any} node
	 */
	function clickOutside(node) {
		const handleClick = (/** @type {any} */ event) => {
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
		open = !open;
	}
</script>

<header id="">
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
			class="burger-button nav-area"
			role="button"
			aria-roledescription="Opens the navigation"
			on:click={toggleBurgerNav}
			on:keydown={toggleBurgerNav}
		>
			<img src={burger} alt="Burger Button" />
		</div>

		<ul
			class="nav-links nav-area"
			use:clickOutside
			on:outclick={() => (open = false)}
			class:active={open}
		>
			<li><a class="contrast nav-link" href="/about">Sobre Nós</a></li>
			<li><a class="contrast nav-link" href="/roda-de-cura">Roda de Cura</a></li>
			<li><a class="contrast nav-link" href="/dallet">Dallet</a></li>
			<li><a class="contrast nav-link" href="/contact">Contate-nos</a></li>
		</ul>
	</nav>
</header>

<slot />

<footer>
	<div class="container">
		<br />
	</div>
</footer>

<style>
	header {
		z-index: 15;
		background-color: var(--primary);
		color: var(--primary-inverse);
		position: fixed;
		top: 0;
		width: 100%;
	}

	header * {
		font-size: 18pt;
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
			background-color: var(--primary);
			display: flex;
			flex-direction: column;
			position: fixed;
			top: 10%;
			right: 0;
			padding: 0 30px 0 25px;
			border-radius: 0 0 var(--border-radius) var(--border-radius);
		}

		.burger-button {
			display: flex;
			margin: auto 0;
		}
	}
</style>
