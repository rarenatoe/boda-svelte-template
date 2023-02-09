<script>
	import Counter from './Counter.svelte';
	import CloudySVG from '$lib/images/cloudy.svg';
</script>

<svelte:head>
	<title>Reni & Deni: Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section id="portada">
	<div id="content">
		<h3>Nos casaremos</h3>
		<h1 id="title">Denisse & Renato</h1>
		<h3>18 de Marzo del 2023</h3>
		<Counter />
		<button id="donde">Donde</button>
	</div>
	<img src={CloudySVG} alt="nubes" width="100%" color="#FEE6EA" />
</section>
<section>
	<div class="square" />
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

	section .square {
		display: flex;
		height: 100%;
		width: 100%;
		max-width: 300px;
		margin: 2rem;
	}

	#portada {
		padding: 0;
		background-image: url('../lib/images/portada.jpeg');
		background-size: cover;
		background-attachment: fixed;
		background-repeat: no-repeat;
		background-position: center;
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
		margin: 1rem;
	}

	#address {
		font-family: LibreBaskerville-Regular;
		color: var(--color-theme-0);
		/* text-shadow: inset 0 0 7px 4px #ecacb7; */
		text-shadow: 4px 4px 4px #ae889088;
		padding: 1.2rem;
		padding-bottom: 0px;
		font-size: 14px;
	}
</style>
