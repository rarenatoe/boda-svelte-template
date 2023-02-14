<script>
	import Counter from './Counter.svelte';
	import CloudySVG from '$lib/images/cloudy.svg';
	import portada from '$lib/images/portada.jpg';
	import locacionIcon from '$lib/images/locacion.svg';
</script>

<svelte:head>
	<title>Boda de Renato y Denisse</title>
	<meta
		name="Boda DReni"
		content="App con datos sobre el evento que se llevara a cabo el 18 de marzo"
	/>
</svelte:head>

<section id="portada" style={`background-image: url('${portada}');`}>
	<div id="content">
		<h3>Nos casaremos</h3>
		<h1 id="title">Denisse & Renato</h1>
		<h3>18 de Marzo del 2023</h3>
		<Counter />
		<button id="donde">Donde</button>
	</div>
	<img src={CloudySVG} alt="nubes" width="100%" color="#FEE6EA" />
</section>
<div>
	<div class="menu-item">
		<img src={locacionIcon} alt="informacion del evento" width="64" height="64" />
		Informacion del Evento
	</div>
</div>
<section>
	<iframe
		src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3901.708117068435!2d-76.96358568544079!3d-12.06359269145608!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c76cb0a8c939%3A0x5bd665718c53dc46!2sCasa%20Salcedo%20Eventos!5e0!3m2!1sen!2spe!4v1676340544239!5m2!1sen!2spe"
		width="400"
		height="250"
		style="border:0;"
		loading="lazy"
		referrerpolicy="no-referrer-when-downgrade"
		title="locacion"
	/>
</section>
<section id="address">
	Esperamos poder verte pronto.<br /><br />
	Si deseas bendecirnos con un regalito, puedes dejarlo en cualquiera de las siguientes direcciones:
	<br /> <br />
	- Calle Arnaldo Márquez 853 - Jesús María. <br />
	- Calle Bilbao 157 - Ate. <br /> <br /> <br />
	O virtualmente:
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 3rem;
	}

	.menu-item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex-wrap: wrap;
		color: red;
	}

	.menu-item img {
		color: red;
	}

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

	#content {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	h1,
	h3 {
		color: rgb(243, 243, 243);
		font-weight: 400;
		text-shadow: 4px 4px 4px #b2a9aa;
	}

	h3 {
		font-family: Roboto;
		letter-spacing: 3px;
		text-align: center;
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

	#address {
		font-family: LibreBaskerville-Regular;
		color: var(--color-theme-0);
		text-shadow: 4px 4px 4px #ae889088;
		padding: 1.2rem;
		padding-bottom: 0px;
		font-size: 14px;
	}
</style>
