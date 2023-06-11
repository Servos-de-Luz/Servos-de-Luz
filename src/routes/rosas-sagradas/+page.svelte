<script>
</script>

<svelte:head>
	<title>Rosas Sagradas</title>
</svelte:head>

<section class="empty" />

<section class="founder">
	<div class="container">
		<div class="founder-text">
			<h1>Rosas Sagradas</h1>

			<p>
				O Caminho das Rosas é a simbologia da nossa caminhada espiritual na Terra rumo a Evolução!
				Caminhada esta que muitas vezes está cheia de espinhos, os obstáculos!
			</p>

			<p>
				Estamos aqui para atravessar todas as tempestades da nossa alma, buscando e desenvolvendo o
				nosso desabrochar, o nosso despertar… alcançando o nosso resplendor no qual nos transformará
				em lindas flores, Rosas majestosas no reino do nosso Mestre Yeshua 🌹
			</p>

			<p>
				Em nossa essência mais pura, retornaremos ao nosso lar Celestial. Em união ao todo, nos
				braços do nosso Pai Amado e Mãe Amada🌹 No Oceano Cósmico do amor ✨💫
			</p>

			<p>
				Por que o Caminhos das Rosas? <br />
				Buscamos conhecimento e fé através das Deusas de todos os tempos. Seres Celestiais que nos auxiliam
				com a alegria e plenitude como o perfume das Rosas, porém sendo fortes como os espinhos! Uma
				rosa com espinhos simboliza que a imperfeição faz parte da perfeição, o que envolve nosso aprendizado!
			</p>

			<p>Caminho das Rosas também presente na logo do @servosdeluz 💙</p>

			<p>
				A Rosa Mística nos faz lembrar quem somos e qual nosso propósito aqui na Terra. Além da
				beleza, as rosas vibram em 320 Hertz, uma das flores com o maior padrão vibracional de seu
				reino. Eleva a frequência, nos traz memórias da nossa comunhão com Deus, conhecimento do
				propósito espiritual de todas(os) nós.
			</p>

			<p>
				Nossa Missão: Somos uma irmandade fraternal das @rosas_sagradas em busca da nossa essência,
				buscando nossa cura, para assim sermos instrumentos de amor e luz na caminhada do próximo. A
				fazer de cada momento de nossa vida e missão uma oração. Pois tudo o que fazemos é
				consagrado à Deus Pai e a Deusa Mãe 🌹🙏🏻
			</p>

			<p>
				O tripé de sustentação da nossa caminhada é <br />
				📚Conhecimento (pelo discipulado) <br />
				🧎🏻‍♀fé (pela adoração) <br />
				🧘🏻‍♀Contemplação (pela comunhão)
			</p>
		</div>
		<iframe
			class="founder-instagram"
			title="Instagram"
			src="https://www.instagram.com/rosas_sagradas/embed"
			scrolling="no"
			frameborder="0"
		/>
	</div>
</section>

<section />

<style>
	.founder .container {
		display: flex;
		gap: 2.5rem;
	}

	.founder-text {
		flex: 1.5 1 0;
		display: block;
	}

	.founder-text p:last-child {
		margin: 0;
	}

	.founder-instagram {
		flex: 1 1 0;
		border-radius: var(--border-radius);
	}

	@media (max-width: 900px) {
		section {
			padding-inline: 25px;
		}

		.founder .container {
			gap: 0;
			flex-direction: column;
		}

		.founder-instagram {
			margin-top: 24px;
			border-radius: var(--border-radius);
			width: 100%;
			min-height: 400px;
		}
	}
</style>
