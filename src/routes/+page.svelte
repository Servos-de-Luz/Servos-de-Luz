<svelte:head>
	<meta
		name="description"
		content="A página principal da Servos de Luz, com todos os links para nossas redes sociais e principais
	produtos."
	/>
</svelte:head>
<!-- TODO: Definir um titulo descritivo para a página -->
<title>Servos de Luz, uma comunidade religiosa</title>

<section class="hero">
	<div class="darkener">
		<div class="container hero-text">
			<h1>Servos de Luz</h1>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer elit metus, accumsan in
				orci quis, lobortis cursus felis. Aenean bibendum turpis eget laoreet semper. Nulla
				tincidunt, ante eget blandit eleifend, urna sapien tristique tellus, quis lacinia velit
				magna ac ex. Donec sed risus libero. Maecenas ac cursus lorem, vitae tincidunt ante. Mauris
				venenatis lobortis feugiat. Nam diam leo, dapibus ut nisl sit amet, imperdiet lobortis
				lacus...
			</p>
			<a href="/about" role="button" class="secondary">Leia Mais</a>
		</div>
	</div>
</section>

<section class="services">
	<div class="container">
		<h2>Nossos Serviços</h2>
		<div class="services-container">
			<div>
				<img class="service-img" src="https://source.unsplash.com/random/500x500/?a" alt="" />
				<div class="service-description">
					<h3>Roda de Cura</h3>
					<p>
						A Roda de Cura Sagrada é uma cerimônia onde os participantes se reúnem para receberem a
						cura espiritual, mental e física. Momento de abrir o coração, deixando ir todas as dores
						e vivenciar as forças do Sagrado.
					</p>
					<a role="button" class="outline secondary" href="/roda-de-cura">Saiba Mais</a>
				</div>
			</div>

			<div>
				<img class="service-img" src="https://source.unsplash.com/random/500x500/?A" alt="" />
				<div class="service-description">
					<h3>Serviço 2</h3>
					<p>
						Morbi tristique senectus et netus. Consectetur lorem donec massa sapien faucibus et
						molestie. Aliquet eget sit amet tellus cras adipiscing enim eu. Venenatis tellus in
						metus vulputate eu.
					</p>
					<a role="button" class="outline secondary" href="/roda-de-cura">Saiba Mais</a>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="Depoimentos" />

<style lang="scss">
	* {
		box-sizing: border-box;
	}

	section.hero {
		background-image: url('https://images.unsplash.com/photo-1521728935364-00584c026397?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=1080&w=2600');

		.darkener {
			backdrop-filter: blur(5px);
			background-color: var(--primary-focus);
		}
	}

	.hero-text {
		padding-block: 7rem;
		text-align: center;

		* {
			margin-bottom: 1.5rem;
		}

		h1 {
			font-size: 3em;
			font-weight: 400;
			color: var(--secondary);
		}

		p {
			padding-inline: 3rem;
			text-align: justify;
		}

		@media screen and (min-width: 768px) {
			p {
				padding-inline: 10rem;
			}
		}
	}

	section.services {
		h2 {
			margin-bottom: 1.5rem;
			color: var(--secondary);
		}
	}

	.services-container {
		display: flex;
		justify-content: space-between;

		@media screen and (max-width: 750px) {
			display: block;
		}
	}

	.services-container > div {
		flex: 0 1 45%;
		margin-bottom: 40px;
	}

	.service-description > a[role='button'] {
		align-self: flex-end;
	}

	@media screen and (max-width: 600px) {
		.services-container > div {
			flex: 0 1 100%;
		}
	}

	.service-img {
		border-radius: var(--border-radius);
		margin-bottom: 0.75rem;
	}

	.service-description {
		margin: 0 auto;

		h3 {
			margin-bottom: 0.75rem;
		}

		p {
			text-align: justify;
		}

		a {
			width: 100%;
			margin-bottom: 0.75rem;
		}
	}
</style>
