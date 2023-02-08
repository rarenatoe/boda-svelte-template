<script>
	import Counter from './Counter.svelte';
</script>

<svelte:head>
	<title>Reni & Deni: Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="section1">
	<div class="container">
		<h3 id="pre-title">Nos casaremos</h3>
		<h1 id="title">Denisse & Renato</h1>
		<h3 id="fecha">18 de Marzo del 2023</h3>
		<div id="counter">
			<Counter />
		</div>
		<div id="button">
			<button id="donde">Donde</button>
		</div>
		
		<!-- <div class= "address">Esperamos poder verte pronto.<br><br>
		Si deseas bendecirnos con un regalito, puedes dejarlo en cualquiera de las siguientes direcciones: <br> <br>
		- Calle Arnaldo Márquez 853 - Jesús María. <br>
		- Calle Bilbao 157 - Ate.  <br> <br> <br> 
		O virtualmente:</div> -->
	</div>
	<div class="elementor-shape"></div>
	<div></div>
		
		

	
	
</section>
<!-- <section class="section2">
	<div class="cuadrado">
		Nuestra historia
	</div>

</section> -->

<style>

	h1 {
		width: 100%;
	}

	.section1 {
		align-self: auto;
		background-attachment: fixed;
		background-image: url(../lib/images/PORTADA.jpeg);
		background-size: cover;
		box-sizing: border-box;
		color: rgb(122, 122, 122);
		display: block;
		flex-basis: auto;
		flex-grow: 0;
		flex-shrink: 1;
		font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
		font-size: 16px;
		font-weight: 300;
		height: 342.781px;
		hyphens: manual;
		line-height: 25.6px;
		order: 0;
		overflow-wrap: break-word;
		position: relative;
		text-size-adjust: 100%;
		max-width: 1200px;
		min-height: 800px;
		/* flex-direction: column;
		justify-content: center;
		align-items: center;
		position: relative;
		
		background-position: center center;
		 */
		
	}


	#pre-title{
		box-sizing: border-box;
		clear: both;
		color: rgb(243,243,243);
		display: block;
		font-family: Roboto; /*cambiar*/
		font-weight: 400;
		height: 27.1953px;
		letter-spacing: 3px;
		line-height: 27.2px;
		overflow-wrap: break-word;
		text-align: center;
		text-size-adjust: 100%;
		vertical-align: baseline;
		width: 1070px;
		text-shadow: 4px 4px 4px #b2a9aa;


	}
	#title {
		color: rgb(243,243,243);
		display: block;
		font-family: AdlerySwash;
		font-size: 110px;
		font-style: normal;
		font-weight: 400;
		height: 132px;
		line-height: 132px;
		margin: 0;
		overflow-wrap: break-word;
		text-align: center;
		text-size-adjust: 100%;
		vertical-align: baseline;
		width: 1102px;


		/* color: var(--color-theme-1); */
		/* text-shadow: inset 0 0 7px 4px #ecacb7; */
		text-shadow: 4px 4px 4px #b2a9aa;
		/* opacity: 1; */
	}

	#fecha{
		box-sizing: border-box;
		clear: both;
		color: rgb(243,243,243);
		display: block;
		font-family: RobotoSlab-Regular; /*cambiar*/
		font-size: 40px;
		font-weight: 400;
		height: 27.1953px;
		letter-spacing: 3px;
		line-height: 27.2px;
		overflow-wrap: break-word;
		text-align: center;
		text-size-adjust: 100%;
		vertical-align: baseline;
		width: 1070px;
		text-shadow: 4px 4px 4px #b2a9aa;

	}

	#counter{
		color:  rgb(243,243,243);
		text-shadow: 4px 4px 4px #b2a9aa;
	}

	#button{
		align-content: normal;
		align-items: normal;
		align-self: auto;
		box-sizing: border-box;
		color: rgb(122, 122, 122);
		display: block;
		flex-basis: auto;
		position: relative;
		flex-direction: row;
		flex-grow: 0;
		flex-shrink: 1;
		flex-wrap: nowrap;
		font-size: 16px;
		font-style: normal;
		font-weight: 300;
		height: 115px;
		hyphens: manual;
		justify-content: manual;
		line-height: 25.6px;
		order: 0;
		overflow-wrap: break-word;
		position: relative;
		text-align: center;
		text-size-adjust: 100%;
		vertical-align: baseline;
		width: 1102px;

	}


	#donde{
		font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
		background-color: rgb(255,255,255,0);
		border-bottom-width: 1px;
		border-left-width: 1px;
		border-right-width: 1px;
		border-top-width: 1px;
		box-shadow: none;
		box-sizing: border-box;
		color: rgb(243,243,243);
		font-size: 11px;
		font-style: normal;
		font-weight: 400;
		height: 45px;
		hyphens: manual;
		letter-spacing: 4px;
		line-height: 11px;
		overflow-wrap: break-word;
		padding-bottom: 16px;
		padding-left: 32px;
		padding-right: 32px;
		padding-top: 16px;
		text-align: center;
		text-decoration-color: rgb(243,243,243) ;
		text-decoration-line: none ;
		text-decoration-style: solid ;
		text-decoration-thickness: auto;
		text-size-adjust: 100%;
		vertical-align: baseline;
		width: 149.953px;
		text-transform: uppercase;
		text-shadow: 4px 4px 4px #b2a9aa;



	}
	.address {
		font-family: LibreBaskerville-Regular;
		color: var(--color-theme-0);
		/* text-shadow: inset 0 0 7px 4px #ecacb7; */
		text-shadow: 4px 4px 4px #ae889088;
		padding: 1.2rem;
		padding-bottom: 0px;
		font-size: 14px;
	}

	.container {
		/* align-content: center; */
		align-items: center;
		box-sizing: border-box;
		color: rgb(122,122,122);
		display: flex;
		flex-wrap: wrap;
		font-size: 16px;
		font-weight: 300;
		height: 400.195px;
		hyphens: manual;
		justify-content: center;
		line-height: 25.6px;
		overflow-wrap: break-word;
		position: relative;
		text-size-adjust: 100% ;
		vertical-align: baseline;
		width: 1102px;

	}

	
</style>
