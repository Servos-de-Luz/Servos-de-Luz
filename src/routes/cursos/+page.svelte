<script>
	import akashicos from '$lib/assets/cursos/akashicos.webp';
	import caminhorosas from '$lib/assets/cursos/caminhorosas.webp';
	import regressao from '$lib/assets/cursos/regressao.webp';
</script>

<svelte:head>
	<title>Cursos</title>
</svelte:head>

<section class="empty" />

<section class="cursos">
	<div class="container">
		<h1>Cursos</h1>

		<div class="cursos-lista">
			<div class="curso-item">
				<img src={akashicos} alt="" />
				<div>
					<p>
						Como uma ferramenta de Cura, os Registros Akáshicos, além de expandir a consciência
						proporciona uma transformação do ser humano com questões relacionadas ao passado,
						presente e futuro. Refletindo nos relacionamentos pessoais, no profissional, na
						prosperidade, saúde física, emocional e espiritual.
						<br /> <br />

						- Identificando traumas, resistências e bloqueios conscientes e inconscientes. <br />
						- Entendimento do porquê de algumas situações emocionais e comportamentos se repetirem.
					</p>
					<a
						class="outline"
						href="https://hotmart.com/pt-br/marketplace/produtos/curso-de-formacao-em-registros-akashicos/K54065083W?sck=HOTMART_PRODUCT_PAGE"
						role="button"
						target="_blank"
						rel="noopener noreferrer">Saiba Mais</a
					>
				</div>
			</div>
			<div class="curso-item">
				<img src={caminhorosas} alt="" />
				<div>
					<p>
						O Curso CAMINHO DAS ROSAS, é um momento Sagrado para reconexão e fortalecimento
						espiritual. Através de estudos e práticas e além de aprender a fazer o seu próprio
						Rosário de pétalas de Rosas, também irá encontrar o caminho de reconexão com a
						ancestralidade. <br />
						O Curso traz a iniciação com teoria e prática para transformação na vida. Com fortalecimento
						e amor. O Rosário também pode ser feito para presentearmos quem amamos, como um amuleto poderoso,
						e para a confecção de terços para vender, trazendo uma excelente rentabilidade financeira.
					</p>
					<a
						class="outline"
						href="https://hotmart.com/pt-br/marketplace/produtos/rosario-das-deusas/U82002730Y?sck=HOTMART_PRODUCT_PAGE"
						role="button"
						target="_blank"
						rel="noopener noreferrer">Saiba Mais</a
					>
				</div>
			</div>
			<div class="curso-item">
				<img src={regressao} alt="" />
				<div>
					<p>
						Você é a soma de todas as experiências. Quanto maiores os conhecimentos e a compreensão
						sobre a vida, mais perto você estará da sua liberdade. A regressão de vidas passadas não
						é um método mágico, que tudo cura, mas sim um instrumento que ajuda a transformar o seu
						eu. O que fizemos ontem influenciou o nosso hoje. o que fazemos hoje, influenciará o
						nosso amanhã. Esse curso te passará um instrumento valioso para melhorar sua qualidade
						de vida. Assim como libertação de traumas e bloqueios adquiridos em outras vidas. Quanto
						mais cuidado e exatidão você tiver na utilização do Processo, maiores serão os
						benefícios. Conheça-te a ti mesmo. Entre nessa jornada de expansão da consciência para
						si mesmo e para ajudar a outras pessoas.
					</p>
					<a
						class="outline"
						href="https://hotmart.com/pt-br/marketplace/produtos/regressao-de-vidas-passadas/R57744325O?sck=HOTMART_PRODUCT_PAGE"
						role="button"
						target="_blank"
						rel="noopener noreferrer">Saiba Mais</a
					>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.cursos-lista {
		& > :nth-child(odd) {
			flex-direction: row-reverse;
			margin: var(--block-spacing-vertical) 0;
		}
	}

	.curso-item {
		display: flex;
		gap: 2.5rem;

		@media screen and (max-width: 768px) {
			flex-direction: column !important;
		}

		& > img {
			border-radius: var(--border-radius);
		}

		& p {
			text-align: justify;
			overflow: hidden;
			display: -webkit-box;
			-webkit-line-clamp: 6; /* number of lines to show */
			line-clamp: 6;
			-webkit-box-orient: vertical;
		}

		& > div {
			display: flex;
			flex-direction: column;
			justify-content: space-between;
		}
	}
</style>
