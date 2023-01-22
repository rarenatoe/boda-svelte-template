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
	<div>Esperamos poder verte pronto</div>
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
		color: #d95b71;
		/* text-shadow: inset 0 0 7px 4px #ecacb7; */
		text-shadow: 4px 4px 4px #ecacb7;
		opacity: 1;
	}
</style>
