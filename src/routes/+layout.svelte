<script lang="ts">
	import '@picocss/pico';
	import '../app.css';

	// FIXME: Make logo_sm 5% bigger
	import logo from '$lib/assets/logo_nobg_sm.webp';

	import whatsapp from '$lib/assets/icons/whatsapp.svg';
	import instagram from '$lib/assets/icons/instagram.svg';
	import youtube from '$lib/assets/icons/youtube.svg';
	import { page } from '$app/stores';
</script>

<header>
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
			<li><a href="#" class="nav-link"><img src={whatsapp} alt="Whatsapp Link" /></a></li>
			<li>
				<a href="https://www.instagram.com/servosdeluz" target="_blank" class="nav-link"
					><img src={instagram} alt="Instagram Link" /></a
				>
			</li>
			<li>
				<a href="https://www.youtube.com/@ServosdeLuz" target="_blank" class="nav-link"
					><img src={youtube} alt="Youtube Link" /></a
				>
			</li>
		</ul>
	</nav>
</header>

<slot />

<footer>
	<div class="container">
		<br />
	</div>
</footer>

<style lang="scss">
	/* .hero {
		background-color: #394046;
		background-image: url(https://source.unsplash.com/random/1920x1080/?white);
		background-position: center;
		background-size: cover;
	} */

	header,
	footer {
		background-color: var(--primary);
		color: var(--primary-inverse);
		position: sticky;
		top: 0;
	}

	header * {
		color: var(--primary-inverse);
	}

	#page-logo {
		cursor: pointer;
		border-radius: 15px;
		width: 72px;

		&:hover {
			transition: 65ms;
			transform: scale(105%);
		}
	}

	.nav-link {
		width: 48px;
		transition: 65ms;

		&:hover {
			transition: 65ms;
			transform: scale(125%);
		}
	}
</style>
