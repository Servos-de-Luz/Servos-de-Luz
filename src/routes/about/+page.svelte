<script>
	import rejane from '$lib/assets/rejane.webp';
</script>

<section class="empty" />

<section class="founder">
	<div class="container">
		<div class="founder-text">
			<h1>Minha Jornada</h1>
			<p>
				Meu nome é Rejane Oliveira, minha trajetória iniciou aos 20 anos, quando iniciei os estudos
				em uma Casa Espírita, desenvolvendo e entendendo a mediunidade, essa abertura de comunicação
				entre os dois mundos.
			</p>
			<p>
				Nos últimos 27 anos do meu caminhar, continuei em estudos, práticas mediúnicas,
				atendimentos, psicografias, retiros espirituais, e como dirigente em cursos e iniciações no
				caminho místico para todas as pessoas com o despertar espiritual. No lado terreno sou
				Psicóloga Clínica com bacharelado e licenciatura, advogada pela OAB do DF, e terapeuta em
				Thetahealing
			</p>
			<p>
				Iniciei a Caminhada com os SERVOS DE LUZ em 2017, recebendo os guias amigos espirituais
				Gabriel, Ísis e Akim! Iniciamos os encontros do Evangelho de Luz todas as segundas-feiras!
				Com o mentor espiritual AKIM, iniciei os estudos e projetos para a Gravação DALET🌀
				@ressonantesdalet.
			</p>
			<p>
				Em 2020 iniciamos a prática espiritual presencial e em 2021 a Roda de Cura Sagrada💚
				@rodadecura.sagrada.
			</p>
			<p>
				Em 2022, iniciei a Caminhada das Rosas com estudo para iniciação das Servas de Madalena. O
				Sagrado Feminino! Iniciando também a caminhada Mística com o Rosário das Deusas de Pétalas
				de Rosa 🌹
			</p>

			<p>Em 2023 iniciei a construção física do Templo na Casa Servos de Luz!</p>

			<p>
				E atualmente nas redes sociais ministrando palestras e cursos para o autodesenvolvimento e
				evolução espiritual! Sejam bem-vindos nessa caminhada de amor com os Servos de Luz 💙🌀
				@servosdeluz e as @rosas_sagradas 🌹
			</p>

			<p>
				Veja mais em meu <a
					href="https://www.instagram.com/rosas_sagradas/"
					target="_blank"
					rel="noopener noreferrer">instagram</a
				>.
			</p>
		</div>
		<img
			class="founder-img"
			src={rejane}
			alt="Rejane sentada em uma cadeira no espaço da roda de cura"
		/>
	</div>
</section>

<section class="about">
	<div class="container">
		<h1>Sobre Nós</h1>

		<h3>Missão</h3>
		Promover o estudo, a prática e a difusão da Doutrina Espírita-Cristã, por meio da vivência do amor
		e da caridade, contribuindo para a evolução da humanidade encarnada e desencarnada.

		<br />

		<h3>Visão</h3>
		Ser uma Instituição Espiritual Universalista, acolhendo a todos que a buscam e prestando serviços
		de qualidade para a comunidade, auxiliando na evolução moral para a construção de uma sociedade mais
		justa e solidária.

		<br />

		<div class="two-columns">
			<div>
				<h3>Valores Servos de Luz</h3>
				<ul class="multi-list">
					<li>Amor</li>
					<li>Caridade</li>
					<li>Comprometimento</li>
					<li>Cooperação</li>
					<li>Disciplina</li>
					<li>Empatia</li>
					<li>Fé</li>
					<li>Fraternidade</li>
					<li>Honestidade</li>
					<li>Respeito</li>
					<li>Tolerância</li>
				</ul>
			</div>

			<div>
				<h3>Princípios</h3>
				<ul class="multi-list">
					<li>Atendimento impessoal</li>
					<li>Ética</li>
					<li>Pureza Doutrinária</li>
					<li>Renovação (formação de colaboradores e sucessores)</li>
					<li>Responsabilidade Espiritual e Sócio-Ambiental</li>
					<li>Trabalho em Equipe</li>
					<li>Transparência</li>
					<li>União</li>
				</ul>
			</div>
		</div>
	</div>
</section>

<style>
	.founder .container {
		display: flex;
		align-items: center;
		gap: 2.5rem;
	}

	.founder-text {
		flex: 1.5 1 0;
		display: block;
	}

	.founder-text p:last-child {
		margin: 0;
	}

	.founder-img {
		flex: 1 1 0;
		border-radius: var(--border-radius);
		width: 25%;
	}

	@media (max-width: 900px) {
		.founder .container {
			gap: 0;
			flex-direction: column;
		}

		.founder-img {
			border-radius: var(--border-radius);
			width: 100%;
		}
	}

	.about h1,
	.about h3 {
		margin-block: 1.5rem;
	}

	.two-columns {
		display: flex;
		justify-content: space-between;
	}

	/* small screen */
	@media (max-width: 990px) {
		.two-columns {
			flex-direction: column;
		}
	}
</style>
