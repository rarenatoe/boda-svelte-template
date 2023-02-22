<script lang="ts">
	import copy from 'clipboard-copy';
	import copyIcon from '$lib/images/copy.svg';
	import { toast } from '@zerodevx/svelte-toast';

	import './styles.css';

	export let code: string;
	export let skipCleanUp: boolean = false;

	const onClick = () => {
		if (skipCleanUp) copy(code);
		else {
			const curatedCode = code.replace(/[^a-zA-Z0-9 ]/g, '');
			copy(curatedCode);
		}
		toast.push('Código copiado al portapapeles');
	};
</script>

<button class="copy-code" on:click={onClick}>
	<code>{code}</code> <img src={copyIcon} alt="copy" />
</button>

<style>
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
