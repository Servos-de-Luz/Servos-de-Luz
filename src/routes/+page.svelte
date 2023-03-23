<svelte:head>
	<meta
		name="description"
		content="A página principal da Servos de Luz, com todos os links para nossas redes sociais e principais
	produtos."
	/>
</svelte:head>
<!-- TODO: Definir um titulo descritivo para a página -->
<title>Servos de Luz, uma comunidade religiosa</title>

<main>
	<section class="hero">
		<div class="darkener">
			<div class="container hero-text">
				<h1>Servos de Luz</h1>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer elit metus, accumsan in
					orci quis, lobortis cursus felis. Aenean bibendum turpis eget laoreet semper. Nulla
					tincidunt, ante eget blandit eleifend, urna sapien tristique tellus, quis lacinia velit
					magna ac ex. Donec sed risus libero. Maecenas ac cursus lorem, vitae tincidunt ante.
					Mauris venenatis lobortis feugiat. Nam diam leo, dapibus ut nisl sit amet, imperdiet
					lobortis lacus.
				</p>
				<a href="/about" role="button" class="secondary">Leia Mais</a>
			</div>
		</div>
	</section>

	<section>
		<div class="services container">
			<h2>Nossos Serviços</h2>
			<div class="services-container">
				<div>
					<img src="https://source.unsplash.com/random/500x500/?" alt="" />
					<div>
						<h3>Serviço 1</h3>
					</div>
				</div>
				<div>
					<img src="https://source.unsplash.com/random/500x500" alt="" />
					<div>
						<h3>Serviço 1</h3>
					</div>
				</div>
			</div>
		</div>
	</section>

	<section class="Depoimentos" />
</main>

<style lang="scss">
	* {
		box-sizing: border-box;
	}

	main {
		background-color: var(--secondary-inverse);
	}

	section.hero {
		background-image: url('https://source.unsplash.com/random/1920x1080/?white');
	}

	.hero .darkener {
		background-color: var(--primary-focus);
	}

	.hero-text {
		padding-block: 8rem;
		text-align: center;

		h1 {
			font-weight: 400;
			margin-block: 0.5rem;
			color: var(--secondary);
		}

		p {
			padding-inline: 10rem;
			text-align: justify;
			margin-bottom: 1.5rem;
			color: var(--secondary);
		}
	}
</style>
