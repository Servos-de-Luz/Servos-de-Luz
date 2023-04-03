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
	<div class="hero-image">
		<div class="container hero-text">
			<h1>Servos de Luz</h1>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer elit metus, accumsan in
				orci quis, lobortis cursus felis...
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

<style>
	* {
		box-sizing: border-box;
	}

	/* HERO SECTION */
	section.hero {
		background: url('https://images.unsplash.com/photo-1521728935364-00584c026397?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=1080&w=2600')
			center/cover;
	}

	.hero-image {
		height: 100vh;
		position: relative;
		backdrop-filter: blur(5px);
		background-color: rgba(0, 0, 0, 0.24);
	}

	.hero-text {
		position: absolute;
		inset: 10% 0 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		color: var(--secondary-inverse);
	}

	.hero-text h1 {
		font-size: 3em;
		font-weight: 400;
		margin-bottom: 1.5rem;
	}

	.hero-text p {
		font-size: larger;
		padding: 0 12rem;
		text-align: justify;
		margin-bottom: 1.5rem;
	}

	@media screen and (max-width: 900px) {
		.hero-text p {
			padding: 0 1rem;
		}
	}

	/* SERVICES SECTION */
	section.services h2 {
		margin-bottom: 1.5rem;
		color: var(--secondary);
	}

	.services-container {
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
	}

	@media screen and (max-width: 750px) {
		.services-container {
			display: block;
		}
	}

	.services-container > div {
		flex: 0 1 calc(45% - 20px);
		margin-bottom: 40px;
	}

	@media screen and (max-width: 600px) {
		.services-container > div {
			flex: 0 1 100%;
		}
	}

	.service-image {
		border-radius: var(--border-radius);
		margin-bottom: 0.75rem;
	}

	.service-description {
		margin: auto;
	}

	.service-description h3 {
		margin-bottom: 0.75rem;
	}

	.service-description p {
		text-align: justify;
		margin-bottom: 0.75rem;
	}

	.service-description a {
		display: inline-block;
		width: 100%;
		margin-bottom: 0.75rem;
	}
</style>
