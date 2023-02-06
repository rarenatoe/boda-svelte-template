<script>
	import Counter from './Counter.svelte';
</script>

<svelte:head>
	<title>Reni & Deni: Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1 class="title">Denisse & Renato</h1>
	<Counter />
	<div class= "address">Esperamos poder verte pronto.<br><br>
		Si deseas bendecirnos con un regalito, puedes dejarlo en cualquiera de las siguientes direcciones: <br> <br>
		- Calle Arnaldo Márquez 853 - Jesús María. <br>
		- Calle Bilbao 157 - Ate.  <br> <br> <br> 
		O virtualmente:</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	h1 {
		width: 100%;
	}

	.title {
		font-family: AdlerySwash;
		color: var(--color-theme-1);
		/* text-shadow: inset 0 0 7px 4px #ecacb7; */
		text-shadow: 4px 4px 4px #ecacb7;
		opacity: 1;
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

	
</style>
