<script lang="ts">
	import copy from 'clipboard-copy';
	import copyIcon from '$lib/images/copy.svg';
	import { toast } from '@zerodevx/svelte-toast';

	import './styles.css';

	export let title: string;
	export let code: string;

	const onClick = () => {
		const curatedCode = code.replace(/[^a-zA-Z0-9 ]/g, '');
		copy(curatedCode);
		toast.push('Código copiado al portapapeles');
	};
</script>

<div class="item">
	<h2>{title}</h2>
	<button class="copy-code" on:click={onClick}>
		<code>{code}</code> <img src={copyIcon} alt="copy" />
	</button>
</div>

<style>
	.item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin: 0 16px;
	}

	.copy-code {
		white-space: nowrap;
		font-size: 16px;
		font-family: var(--font-mono);
		background-color: rgba(255, 255, 255, 0.45);
		border-radius: 3px;
		box-shadow: 2px 2px 6px rgb(255 255 255 / 25%);
		padding: 0.5em;
		overflow-x: auto;
		color: var(--color-text);
		border: none;
	}

	.copy-code:hover {
		filter: brightness(125%);
	}
</style>
