<script>
	import Counter from './Counter.svelte';
	import CodeForCopying from './CodeForCopying.svelte';

	import CloudySVG from '$lib/images/cloudy.svg';
	import infoIcon from '$lib/images/locacion.svg';
	import nosotrosIcon from '$lib/images/nosotros.svg';
	import regalosIcon from '$lib/images/regalos.svg';
	import floresIcon from '$lib/images/flowers.svg';
	import portada from '$lib/images/fotos/centro-escaleras.jpeg';
	import photo1 from '$lib/images/fotos/barranco-oscuras.jpeg';
	import photo2 from '$lib/images/fotos/barranco-pista.jpeg';
	import photo3 from '$lib/images/fotos/centro-alameda-1.jpeg';
	import photo4 from '$lib/images/fotos/centro-alameda-2.jpeg';
	import photo5 from '$lib/images/fotos/centro-pista-1.jpeg';
	import photo6 from '$lib/images/fotos/centro-pista-2.jpeg';
	import photo7 from '$lib/images/fotos/puente-suspiros.jpeg';
	import photo8 from '$lib/images/fotos/barranco-arbol.jpeg';
</script>

<svelte:head>
	<title>Boda de Renato y Denisse</title>
	<meta
		name="Boda DReni"
		content="App con datos sobre el evento que se llevara a cabo el 18 de marzo"
	/>
</svelte:head>

<section id="portada" style={`background-image: url('${portada}');`}>
	<div>
		<h3>Nos casaremos</h3>
		<h1 id="title">Denisse & Renato</h1>
		<h3>18 de Marzo del 2023</h3>
		<Counter />
		<button id="donde">Donde</button>
	</div>
	<img src={CloudySVG} alt="nubes" width="100%" color="#FEE6EA" />
</section>
<section>
	<div id="menu">
		<a class="menu-item" href="#nuestra-historia">
			<img src={nosotrosIcon} alt="informacion del evento" width="64" height="64" />
			Nuestra Historia
		</a>
		<a class="menu-item" href="#info-evento">
			<img src={infoIcon} alt="informacion del evento" width="64" height="64" />
			Informacion del Evento
		</a>
		<a class="menu-item" href="#regalos">
			<img src={regalosIcon} alt="informacion del evento" width="64" height="64" />
			Regalos
		</a>
	</div>
</section>
<section id="nuestra-historia">
	<img src={floresIcon} alt="Flores" width="96" height="96" />
	<h2>Nuestra Historia</h2>

	<p>
		Antes de conocerla, Renato la imaginaba, una musa en su mente que su corazón anhelaba, pero ella
		también lo soñó, el destino así lo quiso, y cuando se conocieron, supieron que ese era el aviso.
	</p>

	<p>
		Fue jugando juegos de mesa donde sus destinos se juntaron, en la casa de Renato, sus caminos se
		encontraron, y desde ese día, cada aventura juntos es única, explorando nuevas cosas, su amor
		crece sin réplica.
	</p>
	<br />

	<div id="photos-grid">
		<img src={photo1} alt="Denisse y Renato en una calle oscura de Barranco" />
		<img src={photo2} alt="Denisse y Renato bailando en la pista de Barranco" />
		<img src={photo3} alt="Denisse y Renato caminando en el Centro de Lima" />
		<img src={photo4} alt="Denisse y Renato mirandose en una alameda del Centro de Lima" />
		<img src={photo5} alt="Denisse y Renato posando en pista del Centro de Lima" />
		<img src={photo6} alt="Denisse y Renato obstruyendo el trafico del Centro de Lima" />
		<img src={photo7} alt="Denisse y Renato en el Puente de los Suspiros" />
		<img src={photo8} alt="Denisse y Renato en Barranco detras de un arbol" />
	</div>
</section>
<section id="info-evento">
	<img src={floresIcon} alt="Flores" width="96" height="96" />
	<h2>Información del Evento</h2>

	<div id="info-grid">
		<div>
			<h3>La Recepción</h3>
			<p>
				18 de Marzo del 2023<br />
				07:00 PM - 08:00 PM<br />
				Casa Salcedo<br />
				Av. Separadora Industrial 2076<br />
				La Molina
			</p>
		</div>
		<div>
			<h3>Estacionamiento</h3>
			<p>
				Se cuenta con cochera con espacio disponible para autos.<br />
				Contáctanos con tiempo para separarte un espacio.
			</p>
		</div>
		<div>
			<iframe
				src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3901.708117068435!2d-76.96358568544079!3d-12.06359269145608!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c76cb0a8c939%3A0x5bd665718c53dc46!2sCasa%20Salcedo%20Eventos!5e0!3m2!1sen!2spe!4v1676340544239!5m2!1sen!2spe"
				style="border:0;"
				loading="lazy"
				referrerpolicy="no-referrer-when-downgrade"
				title="locacion"
			/>
		</div>
	</div>
</section>
<section id="regalos">
	<img src={floresIcon} alt="Flores" width="96" height="96" />
	<!-- <img src={regalosIcon} alt="informacion del evento" width="64" height="64" /> -->
	<h2>Regalos</h2>

	<p>
		Si deseas bendecirnos con un regalito, puedes dejarlo en cualquiera de las siguientes
		direcciones:
	</p>
	<ul class="address">
		<li>Calle Arnaldo Márquez 853 - Jesús María.</li>
		<li>Calle Bilbao 157 - Ate.</li>
	</ul>
	<p>O virtualmente:</p>
	<div id="accounts">
		<div>
			<h3>BCP</h3>
			Cta. Soles: <CodeForCopying code="193-75133224-0-44" /><br />
			Yape: <CodeForCopying code="936-864-395" />
		</div>
		<div>
			<h3>Scotiabank</h3>
			Cta. Soles: <CodeForCopying code="150-0278740" /><br />
			Plin: <CodeForCopying code="991-784-082" />
		</div>
		<div>
			<h3>Novios Falabella</h3>
			Codigo: <CodeForCopying code="683167-02" /><br />
			<a href="https://www.noviosfalabella.com.pe/">noviosfalabella.com</a>
		</div>
	</div>
</section>

<style>
	#portada {
		padding: 0;
		background-attachment: fixed;
		background-repeat: no-repeat;
		background-position: center;
		-webkit-background-size: cover;
		-moz-background-size: cover;
		-o-background-size: cover;
		background-size: cover;
		transition: background-image 0.5s ease;
	}

	#portada h1,
	#portada h3 {
		color: rgb(243, 243, 243);
		font-weight: 400;
		text-shadow: 4px 4px 4px #b2a9aa;
	}

	#portada h3 {
		font-family: parrafos;
		letter-spacing: 3px;
		font-size: 1.5rem;
	}

	#title {
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: AdlerySwash;
		height: 132px;
		margin: 0;
	}

	#donde {
		font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
		background-color: rgb(255 255 255 / 10%);
		border-width: 1px;
		color: rgb(243, 243, 243);
		font-size: 0.75rem;
		letter-spacing: 4px;
		padding: 16px 32px;
		text-transform: uppercase;
		text-shadow: 4px 4px 4px #b2a9aa;
		margin: 2rem;
	}

	#menu {
		display: flex;
		flex-direction: row;
		padding: 2rem;
		justify-content: space-evenly;
	}

	.menu-item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		color: var(--color-text);
		padding: 1rem;
		justify-content: flex-start;
		text-align: center;
		font-family: parrafos;
		font-size: 1rem;
		max-width: 128px;
	}

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 2rem;
	}

	section:not(:first-child) > * {
		max-width: 800px;
	}

	p {
		width: 100%;
	}

	section:not(:first-child):nth-child(odd) {
		background-color: white;
	}

	#portada div {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	#photos-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		row-gap: 2rem;
		column-gap: 2rem;
		justify-content: center;
		align-items: center;
		overflow: hidden;
	}

	#photos-grid img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		grid-column: span 2;
	}

	#info-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}

	#info-grid div {
		grid-column: span 2;
		justify-content: center;
		align-items: center;
		text-align: center;
		padding-top: 2rem;
	}

	#regalos {
		font-family: LibreBaskerville-Regular;
		text-shadow: 4px 4px 4px #ae889088;
	}

	#accounts {
		grid-template-columns: 1fr 1fr 1fr;
	}

	#accounts div {
		grid-column: span 3;
		border-bottom: 1px solid black;
		padding-top: 1rem;
		padding-bottom: 1rem;
	}

	@media (min-width: 720px) {
		#photos-grid img {
			grid-column: span 1;
		}

		#accounts {
			display: flex;
			flex-direction: row;
			justify-content: center;
		}

		#accounts :global(.item):not(:first-child) {
			border-left: 1px solid;
		}
	}

	h3 {
		font-family: Titulos;
	}
	h2 {
		font-family: Titulos;
	}
</style>
