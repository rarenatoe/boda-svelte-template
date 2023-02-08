<script>
	import Header from './Header.svelte';
	import './styles.css';
	import Footer from './Footer.svelte';
	import { SvelteToast } from '@zerodevx/svelte-toast';

	// // Optionally set default options here
	// const options = {
	// ...
	// }
</script>

<div class="app">
	<!-- <Header /> -->

	<main>
		<slot />
	</main>

	<SvelteToast
		options={{
			duration: 700,
			intro: { y: 100 },
			dismissable: false,
			theme: {
				'--toastBarHeight': 0
			}
		}}
	/>
	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		/* padding: 1rem; */
		width: 100%;
		/* max-width: 64rem; */
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>
