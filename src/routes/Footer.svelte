<script lang="ts">
	import { toast } from '@zerodevx/svelte-toast';
	import copy from 'clipboard-copy';

	import catEmail from '$lib/images/catemail.png';

	import './styles.css';
	import FooterCell from './FooterCell.svelte';

	const codeOnClick = (code: string) => () => {
		copy(code);
		toast.push('Código copiado al portapapeles');
	};
</script>

<footer>
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

	#cat {
		margin-left: 8px;
	}
</style>
