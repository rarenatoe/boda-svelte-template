<script lang="ts">
	import { toast } from '@zerodevx/svelte-toast';
	import copy from 'clipboard-copy';

	import catEmail from '$lib/images/catemail.png';

	import './styles.css';
	import CodeForCopying from './CodeForCopying.svelte';
	import FooterCell from './FooterCell.svelte';

	const codeOnClick = (code: string) => () => {
		copy(code);
		toast.push('Código copiado al portapapeles');
	};
</script>

<footer>
	<div id="accounts">
		<CodeForCopying title="BCP Cta. Soles" code="193-75133224-0-44" />
		<CodeForCopying title="Scotiabank Cta. Soles" code="150-0278740" />
		<CodeForCopying title="Código de Novios Falabella" code="683167-02">
			<a href="https://www.noviosfalabella.com.pe/">noviosfalabella.com</a>
		</CodeForCopying>
	</div>
	<FooterCell>
		<h2>¿tienes preguntas?</h2>
		<a class="button" href="mailto:rivadeneyradenisse@gmail.com,rare.na.toe@gmail.com">
			Envianos un email <img id="cat" height="20" src={catEmail} alt="cat email" />
		</a>
	</FooterCell>
</footer>

<style>
	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		padding: 2rem;
	}

	a {
		text-align: center;
	}

	@media (min-width: 720px) {
		#accounts {
			display: flex;
			flex-direction: row;
			justify-content: center;
		}

		#accounts :global(.item):not(:first-child) {
			border-left: 1px solid;
		}
	}

	#cat {
		margin-left: 8px;
	}
</style>
