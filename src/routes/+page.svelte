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
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.title {
		font-family: AdlerySwash;
	}
</style>
