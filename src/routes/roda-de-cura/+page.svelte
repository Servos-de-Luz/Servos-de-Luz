<script>
	import cura from '$lib/assets/cura_noblack.webm';

	// @ts-ignore
	function handleHover(e) {
		e.target.playbackRate = 1;
		e.target.play();
	}

	// @ts-ignore
	function handleLeave(e) {
		// Reduce playback rate slowly on mouse leave

		let playbackRates = [0.9, 0.7, 0.5, 0.3, 0.1];
		let delay = 100;

		playbackRates.forEach((rate, index) => {
			setTimeout(() => {
				e.target.playbackRate = rate;
			}, delay * index);
		});

		setTimeout(() => {
			e.target.pause();
		}, delay * playbackRates.length);
	}
</script>

<svelte:head>
	<title>Roda de Cura</title>
</svelte:head>

<div class="empty" />

<section class="map">
	<iframe
		title="Casa Servos de Luz"
		src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1917.5992495590158!2d-48.0877041661549!3d-16.003179099999997!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x935bd52075679ced%3A0x7dd1e388eb676ec2!2sCasa%20Servos%20de%20Luz!5e0!3m2!1spt-BR!2sbr!4v1681218930718!5m2!1spt-BR!2sbr"
		height="300"
		allow="fullscreen"
		style="border:0;"
		loading="lazy"
		referrerpolicy="no-referrer-when-downgrade"
	/>
</section>

<section class="about">
	<!-- Two panels side by side -->
	<div class="container">
		<div class="left">
			<h1>Roda de Cura Sagrada</h1>
			<p>
				A Roda de Cura Sagrada é uma cerimônia onde os participantes se reúnem para receberem a cura
				espiritual, mental e física. Momento de abrir o coração, deixando ir todas as dores e
				vivenciar as forças do Sagrado.
				<br />
				Com trabalhadores/médiuns com suas vibrações espirituais e intenções no momento de doar e atuar
				como instrumentos da espiritualidade! Acontece todo segundo sábado do mês em Brasília!
			</p>

			<iframe
				class="roda-instagram"
				title="Instagram"
				src="https://www.instagram.com/rodadecura.sagrada/embed"
				frameborder="0"
			/>

			<p class="roda-instagram-alt">
				Para mais informações, visite nosso instagram <a
					href="https://www.instagram.com/rodadecura.sagrada/"
					target="_blank"
					rel="noopener noreferrer">@rodadecura.sagrada</a
				>.
			</p>
		</div>
		<div class="right">
			<video
				src={cura}
				loop
				on:mouseenter={handleHover}
				on:mouseleave={handleLeave}
				on:focus={handleHover}
				on:focusout={handleLeave}
				on:click={handleHover}
			>
				<track kind="captions" />
			</video>
		</div>
	</div>
</section>

<style>
	@media (max-width: 900px) {
		section {
			padding-inline: 25px;
		}
	}

	.about .container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 2rem;
	}

	.about .right video {
		width: 100%;
		border-radius: var(--border-radius);
	}

	.map iframe {
		width: 100%;
	}

	.roda-instagram {
		border-radius: var(--border-radius);
		width: 100%;
		height: 207px;
	}

	.roda-instagram-alt {
		display: none;
	}

	/* about media query small device */

	@media (max-width: 900px) {
		.about .container {
			grid-template-columns: 1fr;
		}

		.roda-instagram {
			display: none;
		}

		.roda-instagram-alt {
			display: block;
		}
	}

	h1 {
		margin-bottom: 0.5rem;
	}
</style>
