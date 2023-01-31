<script lang="ts">
	import renyden from '$lib/images/renyden.jpg';

	// const boardGames = [
	// 	'$lib/images/grand-austria-hotel.png',
	// 	'$lib/images/hanabi.png',
	// 	'$lib/images/power-grid.png',
	// 	'$lib/images/race-for-the-galaxy.png',
	// 	'$lib/images/takenoko.webp',
	// 	'$lib/images/netrunner.png',
	// 	'$lib/images/century.png',
	// 	'$lib/images/concordia.png'
	// ];

	const boardGamesPromisesObj = import.meta.glob('$lib/images/boardgames/*');
	// const iterableImages = Object.entries(boardGamesGlob);
	const boardGames = Object.keys(boardGamesPromisesObj);
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<p>Hola, somos Renato y Denisse</p>
<img id="dreni" src={renyden} alt="Renato y Denisse" />

<p>nos gusta los juegos de mesa, como por ejemplo...</p>
<div class="gallery-wrap wrap-effect">
	{#each boardGames as game}
		<div class="item" style={`background-image: url('${game}');`} />
	{/each}
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
		background-position: top;
	}

	/* Image Accordions Effect 2 */

	.wrap-effect .item:hover {
		transform: translate3d(0, 0, 100px);
		filter: saturate(2) contrast(120%);
	}
</style>
