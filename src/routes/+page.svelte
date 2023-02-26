<script lang="ts">
	import Counter from './Counter.svelte';
	import CodeForCopying from './CodeForCopying.svelte';

	import CloudySVG from '$lib/images/cloudy.svg';
	import infoIcon from '$lib/images/locacion.svg';
	import nosotrosIcon from '$lib/images/nosotros.svg';
	import regalosIcon from '$lib/images/regalos.svg';
	import floresIcon from '$lib/images/flowers.svg';
	import cuentaIcon from '$lib/images/cuenta.svg';
	import domicilioIcon from '$lib/images/domicilio.svg';
	import yapeIcon from '$lib/images/yape.png';
	import plinIcon from '$lib/images/plin.png';
	import estacionamientoIcon from '$lib/images/estacionamiento.svg';
	import mapaIcon from '$lib/images/map.svg';
	import recepcionIcon from '$lib/images/recepcion.svg';
	import portada from '$lib/images/fotos/centro-escaleras.jpg';
	import photo1 from '$lib/images/fotos/barranco-oscuras.jpg';
	import photo2 from '$lib/images/fotos/barranco-pista.jpg';
	import photo3 from '$lib/images/fotos/centro-alameda-1.jpg';
	import photo4 from '$lib/images/fotos/centro-alameda-2.jpg';
	import photo5 from '$lib/images/fotos/centro-pista-1.jpg';
	import photo6 from '$lib/images/fotos/centro-pista-2.jpg';
	import photo7 from '$lib/images/fotos/puente-suspiros.jpg';
	import photo8 from '$lib/images/fotos/barranco-arbol.jpg';

	function smoothScroll(event: Event) {
		const id = (event.target as HTMLAnchorElement).getAttribute('href');
		const target = id ? document.querySelector<HTMLElement>(id) : null;
		// const id = event.target?.getAttribute('href');
		// const target = document.querySelector(id);

		if (target) {
			event.preventDefault();
			target.scrollIntoView({
				behavior: 'smooth'
			});
		}
	}
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
		<a id="donde" href="#mapa" on:click|preventDefault={smoothScroll}>Donde</a>
	</div>
	<img src={CloudySVG} alt="nubes" width="100%" color="#FEE6EA" />
</section>
<section>
	<nav>
		<a href="#nuestra-historia" on:click|preventDefault={smoothScroll}>
			<img src={nosotrosIcon} alt="informacion del evento" />
			Nuestra Historia
		</a>
		<a href="#info-evento" on:click|preventDefault={smoothScroll}>
			<img src={infoIcon} alt="informacion del evento" />
			Informacion del Evento
		</a>
		<a href="#regalos" on:click|preventDefault={smoothScroll}>
			<img src={regalosIcon} alt="informacion del evento" />
			Regalos
		</a>
	</nav>
</section>
<section id="nuestra-historia">
	<img src={floresIcon} alt="Flores" />
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
	<img src={floresIcon} alt="Flores" />
	<h2>Información del Evento</h2>

	<div class="trio-grid" id="info-grid">
		<div>
			<img src={recepcionIcon} alt="Recepcion" width="60" height="60" />
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
			<img src={estacionamientoIcon} alt="Estacionamiento" width="60" height="60" />
			<h3>Estacionamiento</h3>
			<p>
				Se cuenta con cochera con <br /> espacio disponible para autos.<br />
				Contáctanos con tiempo<br />
				para separarte un espacio.
			</p>
		</div>
		<div id="mapa">
			<div>
				<img src={mapaIcon} alt="Mapa" width="60" height="60" />
				<h3>Mapa</h3>
			</div>
			<div>
				<iframe
					src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3901.708117068435!2d-76.96358568544079!3d-12.06359269145608!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c76cb0a8c939%3A0x5bd665718c53dc46!2sCasa%20Salcedo%20Eventos!5e0!3m2!1sen!2spe!4v1676340544239!5m2!1sen!2spe"
					style="border:0;"
					width="100%"
					height="100%"
					loading="lazy"
					referrerpolicy="no-referrer-when-downgrade"
					title="locacion"
				/>
			</div>
		</div>
	</div>
</section>
<section id="regalos">
	<img src={floresIcon} alt="Flores" />
	<h2>Regalos</h2>
	<div class="trio-grid">
		<div id="domicilio">
			<h3>A domicilio</h3>
			<p>
				Si deseas bendecirnos con un regalito, puedes dejarlo en cualquiera de las siguientes
				direcciones:
			</p>
			<ul>
				<li>Calle Arnaldo Márquez 853 - Jesús María.</li>
				<li>Calle Bilbao 157 - Ate.</li>
			</ul>
			<p>O virtualmente:</p>
		</div>
		<div>
			<h3>Novios Falabella</h3>
			Codigo: <CodeForCopying code="683167-02" skipCleanUp /><br />
			<a href="https://www.noviosfalabella.com.pe/">noviosfalabella.com</a>
		</div>
		<div id="accounts">
			<h3>Cuentas Bancarias</h3>
			<table>
				<tbody>
					<tr>
						<td>Titular:</td>
						<td><CodeForCopying code="Renato Alegre" /></td>
					</tr>
					<tr>
						<td>BCP Soles:</td>
						<td><CodeForCopying code="193-75133224-0-44" /></td>
					</tr>
					<tr>
						<td><img src={yapeIcon} alt="BCP" /></td>
						<td><CodeForCopying code="936-864-395" /></td>
					</tr>
				</tbody>
			</table>
			<table>
				<tr>
					<td>Titular:</td>
					<td><CodeForCopying code="Denisse Rivadeneyra" /></td>
				</tr>
				<tr>
					<td>Scotiabank Soles:</td>
					<td><CodeForCopying code="150-0278740" /></td>
				</tr>
				<tr>
					<td><img src={plinIcon} alt="BCP" /></td>
					<td><CodeForCopying code="991-784-082" /></td>
				</tr>
			</table>
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
		text-shadow: 8px 8px 8px #b2a9aa;
	}

	#portada h3 {
		font-family: parrafos;
		letter-spacing: 3px;
		font-size: 1.5rem;
		margin-top: 1em;
	}

	#title {
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: AdlerySwash;
		margin: 0;
	}

	#donde {
		background-color: rgb(255 255 255 / 10%);
		border-width: 1px;
		color: rgb(243, 243, 243);
		font-size: 0.75rem;
		letter-spacing: 4px;
		padding: 16px 32px;
		text-transform: uppercase;
		text-shadow: 4px 4px 4px #b2a9aa;
		margin: 2rem;
		border-style: outset;
		text-decoration: none;
	}

	#donde:active {
		border: gray 1px solid;
	}

	nav {
		display: flex;
		flex-direction: row;
		padding: 2rem;
		justify-content: space-between;
	}

	nav img {
		width: 4rem;
	}

	nav a {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		color: var(--color-text);
		padding: 1rem;
		justify-content: flex-start;
		text-align: center;
		font-size: 1rem;
		max-width: 128px;
	}

	section:not(:first-child) > * {
		max-width: 800px;
	}
	section:not(:first-child):nth-child(odd) {
		background-color: white;
	}
	section > img:first-child {
		width: 5rem;
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

	.trio-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: auto auto auto;
		column-gap: 2rem;
		row-gap: 2rem;
	}

	.trio-grid div {
		grid-column: span 2;
		text-align: center;
	}

	#domicilio {
		text-align: left;
	}

	#accounts {
		display: grid;
		grid-template-columns: 1fr;
	}
	#accounts > table {
		grid-column: span 1;
		padding: 1rem 0;
	}

	#accounts > table:last-child {
		border-top: 1px solid;
	}

	#accounts img {
		height: 2rem;
		margin-right: 0.5rem;
		vertical-align: middle;
	}

	td {
		text-align: left;
		vertical-align: middle;
	}

	@media (min-width: 720px) {
		#portada h1 {
			font-size: 6rem;
		}

		nav {
			width: 70%;
		}
		nav img {
			width: 5rem;
		}

		nav a {
			font-size: 1.25rem;
		}

		section > img:first-child {
			width: 6rem;
		}

		#photos-grid > img {
			grid-column: span 1;
		}

		.trio-grid {
			grid-template-rows: auto auto;
		}

		.trio-grid > div {
			grid-column: span 1;
		}

		.trio-grid > div:last-child {
			grid-column: span 2;
		}

		#info-grid {
			grid-template-rows: 1fr 1fr 1fr;
		}

		#info-grid #mapa {
			display: grid;
			grid-template-columns: 1fr;
			grid-template-rows: auto 1fr;
			grid-row: span 2;
		}

		#accounts {
			grid-template-columns: 1fr 1fr;
			grid-template-rows: auto 1fr;
		}

		#accounts > *:first-child {
			grid-column: span 2;
		}

		#accounts table {
			padding: 0 1rem;
		}

		#accounts > table:last-child {
			border-top: none;
			border-left: 1px solid;
		}
	}
</style>
