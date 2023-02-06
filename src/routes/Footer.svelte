<script lang="ts">
	import copy from 'clipboard-copy';
	import catEmail from '$lib/images/catemail.png';
	import { toast } from '@zerodevx/svelte-toast';

	import './styles.css';
	import CodeForCopying from './CodeForCopying.svelte';

	const codeOnClick = (code: string) => () => {
		copy(code);
		toast.push('Código copiado al portapapeles');
	};
</script>

<footer>
	<div id="accounts" class="block">
		<CodeForCopying title="BCP Cta. Soles" code="193-75133224-0-44" />
		<CodeForCopying title="Scotiabank Cta. Soles" code="150-0278740" />
		<CodeForCopying title="Código de Novios Falabella" code="683167-02">
			<br><a href="https://www.noviosfalabella.com.pe/">noviosfalabella.com</a>
		</CodeForCopying>
	</div>
	<div class="block">
		<h2>¿tienes preguntas?</h2>
		<a class="button" href="mailto:rivadeneyradenisse@gmail.com,rare.na.toe@gmail.com">
			Envianos un email <img id="cat" height="20" src={catEmail} alt="cat email" />
		</a>
	</div>
</footer>

<style>
	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 16px;
	}

	.block {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	@media (min-width: 720px) {
		#accounts {
			display: flex;
			flex-direction: row;
			align-items: flex-start;
		}
	}

	#cat {
		margin-left: 8px;
	}
</style>
