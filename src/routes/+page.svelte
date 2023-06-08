<script>
	import Carousel from 'svelte-carousel';
	import instagram from '$lib/assets/icons/instagram.svg';
	import whatsapp from '$lib/assets/icons/whatsapp.svg';
	import youtube from '$lib/assets/icons/youtube.svg';
	import telegram from '$lib/assets/icons/telegram.svg';
	import chakra from '$lib/assets/chakra.webp';
	import roda from '$lib/assets/roda.webp';
	import rosas from '$lib/assets/rosas.webp';
	import cursos from '$lib/assets/cursos.webp';
	import { browser } from '$app/environment';
</script>

<svelte:head>
	<meta
		name="description"
		content="A página principal da Servos de Luz, a porta de entrada de nossa comunidade religiosa."
	/>
	<title>Servos de Luz, uma comunidade religiosa</title>
</svelte:head>

<section class="hero">
	<div class="hero-image">
		<div class="container hero-text">
			<h1>Servos de Luz</h1>
			<p>Uma nova era de mediunidade em Brasília.</p>
			<ul class="contacts">
				<li class="contact">
					<a href="https://www.instagram.com/servosdeluz/" target="_blank" rel="noopener noreferrer"
						><img src={instagram} alt="link para o instagram" /></a
					>
				</li>
				<li class="contact">
					<a
						href="https://chat.whatsapp.com/DpICwCKwV3lCq5igs46hPw"
						target="_blank"
						rel="noopener noreferrer"><img src={whatsapp} alt="link para o whatsapp" /></a
					>
				</li>
				<li class="contact">
					<a href="https://t.me/servosdeluzz" target="_blank" rel="noopener noreferrer"
						><img src={telegram} alt="link para o whatsapp" /></a
					>
				</li>
				<li class="contact">
					<a
						href="https://www.youtube.com/channel/UCI8mUUSl4HDviPwYz7MWdpA"
						target="_blank"
						rel="noopener noreferrer"><img src={youtube} alt="link para o youtube" /></a
					>
				</li>
			</ul>
			<a href="/about" role="button" class="primary">Quem Somos</a>
		</div>
	</div>
</section>

<section class="services">
	<div class="container">
		<h2>Nossos Serviços</h2>
		<div class="services-container">
			<div>
				<img class="service-img" src={roda} alt="" />
				<div class="service-description">
					<h3>Roda de Cura</h3>
					<p>
						A Roda de Cura Sagrada é uma cerimônia onde os participantes se reúnem para receberem a
						cura espiritual, mental e física. Momento de abrir o coração, deixando ir todas as dores
						e vivenciar as forças do Sagrado.
					</p>
					<a role="button" class="outline" href="/roda-de-cura">Saiba Mais</a>
				</div>
			</div>

			<div>
				<img class="service-img" src={chakra} alt="" />
				<div class="service-description">
					<h3>Gravações Dalet</h3>
					<p>
						Uma ferramenta de crescimento, no autodesenvolvimento e evolução do físico, emocional,
						mental e espiritual que auxilia na expansão da consciência para uma jornada produtiva em
						todas os aspectos na vida.
					</p>
					<a role="button" class="outline" href="/dalet">Saiba Mais</a>
				</div>
			</div>
		</div>
		<div class="services-container">
			<div>
				<img class="service-img" src={rosas} alt="" />
				<div class="service-description">
					<h3>Rosas Sagradas</h3>
					<p>
						A Roda de Cura Sagrada é uma cerimônia onde os participantes se reúnem para receberem a
						cura espiritual, mental e física. Momento de abrir o coração, deixando ir todas as dores
						e vivenciar as forças do Sagrado.
					</p>
					<a role="button" class="outline" href="/rosas-sagradas">Saiba Mais</a>
				</div>
			</div>

			<div>
				<img class="service-img" src={cursos} alt="" />
				<div class="service-description">
					<h3>Outros Cursos</h3>
					<p>
						Uma ferramenta de crescimento, no autodesenvolvimento e evolução do físico, emocional,
						mental e espiritual que auxilia na expansão da consciência para uma jornada produtiva em
						todas os aspectos na vida.
					</p>
					<a role="button" class="outline" href="/cursos">Saiba Mais</a>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="depoimentos">
	<div class="container">
		<h2>Depoimentos</h2>
		<div class="depoimentos-container">
			{#if browser}
				<Carousel autoplay autoplayDuration={10000} swiping={false}>
					<div class="depoimento">
						<cite>
							Ontem eu estava com tantas dores no corpo, uma tremedeira, mal estar e a medida que
							foi iniciado o decreto, fui melhorando e quando finalizou que bebi a água... senti um
							alívio enorme e a dor passou. Muito bom e vamos seguindo nesse processo de cura e
							despertar espiritual. Obrigada <a
								href="https://www.instagram.com/servosdeluz/"
								target="_blank"
								rel="noopener noreferrer">@servosdeluz</a
							>.

							<br />
							-
							<a
								href="https://www.instagram.com/stories/highlights/17895965026679372/"
								target="_blank"
								rel="noopener noreferrer">mamelo3574</a
							>
						</cite>
					</div>
					<div class="depoimento">
						<cite>
							Amém, gratidão!! Realmente o evangelho do lar dos servos de luz é maravilhoso!! Eu ja
							o faço há uns 4 meses, como as coisas mudaram em minha vida, sou muito grata a Jesus ,
							a Regina e aos servos de luz!!!
							<br />
							-
							<a
								href="https://www.instagram.com/stories/highlights/18047196073167733/"
								target="_blank"
								rel="noopener noreferrer">Anônimo</a
							>
						</cite>
					</div>
					<div class="depoimento">
						<cite>
							Eu fiz o mesmo no evangelho do dia 02/12... coloquei que queria um trabalho até 20/12,
							pois queria começar o ano trabalhando. Hoje depois de 6 meses desempregada recebi um
							resposta positiva e começo a trabalhar segunda-feira. Obrigada Re e todos do servo de
							luz por nos ajudar a não desistir e por todos os ensinamentos... sou muito muito
							Grata!!!!!!
							<br />
							-
							<a
								href="https://www.instagram.com/stories/highlights/17876774128486047/"
								target="_blank"
								rel="noopener noreferrer">Anônimo</a
							>
						</cite>
					</div>
				</Carousel>
			{/if}
		</div>
	</div>
</section>

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

		& h1 {
			font-size: 3em;
			font-weight: 400;
			margin-bottom: 1.5rem;
			text-shadow: 0px 0px 15px rgba(0, 0, 0, 0.4);
			color: var(--secondary-inverse);
		}

		& p {
			font-size: larger;
			padding: 0 12rem;
			text-align: justify;
			margin-bottom: 1.5rem;
			text-shadow: 0px 0px 15px rgba(0, 0, 0, 0.4);
			color: var(--secondary-inverse);
		}
	}

	@media screen and (max-width: 900px) {
		.hero-text p {
			padding: 0 1rem;
		}
	}

	.contacts {
		padding: 0;
		display: flex;
		justify-content: space-between;
		width: 10em;
	}

	.contact {
		border-radius: 100%;
		list-style: none;
		transition: 200ms;

		&:hover {
			transition: 200ms;
			transform: scale(1.3);
			background-color: var(--primary);
		}
	}

	.contact a {
		display: flex;
		align-items: center;
		color: var(--secondary-inverse);
	}

	.contact a img {
		height: 32px;
		width: 32px;
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

	.service-img {
		border-radius: var(--border-radius);
		margin-bottom: 0.75rem;
	}

	.service-description {
		margin: auto;

		& h3 {
			margin-bottom: 0.75rem;
		}

		& p {
			text-align: justify;
			margin-bottom: 0.75rem;
		}

		& a {
			display: inline-block;
			width: 100%;
			margin-bottom: 0.75rem;
		}
	}

	/* DEPOIMENTOS SECTION */

	.depoimentos h2 {
		margin: 0;
	}

	.depoimento {
		display: flex;
		align-items: center;
		padding: 15px;
		min-height: 350px;
	}

	.depoimento cite {
		font-size: 16pt;
		margin: 0;
		padding: 0rem 6rem;
		text-align: justify;
	}

	@media screen and (max-width: 1200px) {
		.depoimentos h2 {
			margin-bottom: 1rem;
		}

		.depoimento cite {
			padding: 0 1rem;
		}
	}
</style>
