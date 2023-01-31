<script lang="ts">
	import renyden from '$lib/images/renyden.jpg';
	type File = { default: string };
	const boardGamesImports = import.meta.glob<{ default: string }>('$lib/images/boardgames/*');

	const boardGamesPromises = Promise.all(
		Object.entries(boardGamesImports).map(async ([path, resolver]) => {
			const { default: imageUrl } = await resolver();
			return {
				imageUrl,
				filename: path.split('/').at(-1) ?? ''
			};
		})
	);
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<p>Hola, somos Renato y Denisse</p>
<img id="dreni" src={renyden} alt="Renato y Denisse" />

<p>nos gusta los juegos de mesa, por ejemplo...</p>
<div class="gallery-wrap wrap-effect">
	{#await boardGamesPromises then boardgames}
		{#each boardgames as game}
			<div class="item" style={`background-image: url('${game.imageUrl}');`} />
		{/each}
	{/await}
</div>

<style>
	#dreni {
		border-radius: 50%;
		padding: 8px;
		height: 40vh;
		width: 40vh;
		object-fit: cover;
		align-self: center;
		filter: brightness(140%);
	}

	.gallery-wrap {
		display: flex;
		flex-direction: row;
		height: 30vh;
	}

	.item {
		flex: 1;
		background-position: center;
		background-size: cover;
		transition: all 0.8s ease;
	}

	.item:hover {
		flex: 8;
	}

	@media (min-width: 720px) {
		.item {
			flex: 4;
		}
	}

	/* Image Accordions Effect 2 */

	.wrap-effect .item:hover {
		transform: translate3d(0, 0, 100px);
		filter: saturate(2) contrast(120%);
	}
</style>
