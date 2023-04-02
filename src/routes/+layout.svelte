<script lang="ts">
	import '@picocss/pico';
	import '../app.css';

	import logo from '$lib/assets/logo_nobg_sm.webp';
	import { page } from '$app/stores';
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
		<ul>
			<li><a class="contrast nav-link" href="/about">Sobre Nós</a></li>
			<li><a class="contrast nav-link" href="/roda-de-cura">Roda de Cura</a></li>
			<li><a class="contrast nav-link" href="/roda-de-cura">Dallet</a></li>
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
		transition: transform 425ms;
	}
</style>
