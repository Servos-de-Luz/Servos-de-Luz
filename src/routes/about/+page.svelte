<script>
	import rejane from '$lib/assets/rejane.webp';
</script>

<section class="empty" />
<section class="about">
	<div class="container">
		<h1>Sobre Nós</h1>
		<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi quam purus, consequat in
			consequat vel, finibus sit amet orci. Aliquam dapibus est quis interdum mattis. Cras eros
			elit, convallis non efficitur sit amet, aliquet non purus. Nunc hendrerit eget nisi eu semper.
			Donec quis commodo lectus. Maecenas et cursus felis. Duis nunc ex, viverra quis imperdiet in,
			volutpat non nunc. Vestibulum ultrices tempus mi. In tristique ultricies nibh, sit amet tempus
			felis volutpat ut.
		</p>
	</div>
</section>
<section class="founder">
	<div class="container">
		<div class="founder-text">
			<h1>Rejane</h1>
			<p>
				Eu sou Rejane, a fundadora do servos de luz. Praesent aliquam varius diam, quis vestibulum
				tellus consectetur eget. Phasellus faucibus justo vitae ullamcorper bibendum. Praesent
				vehicula augue tortor, non hendrerit nisl rhoncus quis. Maecenas sodales in magna ut
				efficitur. Donec ac est vel tellus lobortis molestie. Fusce vel ligula eu erat mollis
				sagittis at id nisi. Sed quis arcu turpis. Pellentesque ullamcorper ante nec commodo auctor.
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
</style>
