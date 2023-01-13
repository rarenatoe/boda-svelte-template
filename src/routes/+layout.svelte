<script>
	import Header from './Header.svelte';
	import copy from 'clipboard-copy';
	import copyIcon from '$lib/images/copy.svg';

	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<div class="block">
			<h2>BCP Cta. Soles</h2>
			<button class="copy-button" on:click={() => copy('19375133224044')}>
				<code>193-75133224-0-44</code>
				<img src={copyIcon} alt="copy" />
			</button>
		</div>
		<div class="block">
			<h2>Scotiabank Cta. Soles</h2>
			<button class="copy-button" on:click={() => copy('1500278740')}>
				<code>150-0278740</code>
				<img src={copyIcon} alt="copy" />
			</button>
		</div>
		<div class="block">
			<h2>Código de Novios Falabella</h2>
			<button class="copy-button" on:click={() => copy('68316702')}>
				<code>683167-02</code>
				<img src={copyIcon} alt="copy" />
			</button>
		</div>
		<div class="mobile-show block">
			<h2>📞 Contáctanos</h2>
			<div class="mini-block">
				<a href="mailto:rivadeneyradenisse@gmail.com"> rivadeneyradenisse@gmail.com</a>
				|
				<a href="mailto:rare.na.toe@gmail.com">rare.na.toe@gmail.com</a>
			</div>
		</div>
	</footer>
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
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 16px;
	}

	footer .block {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-size: 0.8rem;
		margin: 0 16px;
	}

	@media (min-width: 720px) {
		footer .mobile-show {
			display: none;
		}
		footer {
			flex-direction: row;
		}
	}

	.mini-block a {
		margin: 8px 0;
	}

	.copy-button {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	code {
		padding: 0 16px;
	}
</style>
