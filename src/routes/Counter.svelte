<script lang="ts">
	import { onMount } from 'svelte';

	const doubleDigit = (num: number) =>
		Math.floor(num).toLocaleString('en-US', {
			minimumIntegerDigits: 2
		});

	const WEDDING_DAY_MILLISECONDS = +new Date(Date.UTC(2023, 2, 19, 0));
	let millisecondsLeft = WEDDING_DAY_MILLISECONDS - +new Date();

	const SECOND = 1000;
	const MINUTE = SECOND * 60;
	const HOUR = MINUTE * 60;
	const DAY = HOUR * 24;

	$: days = doubleDigit(millisecondsLeft / DAY);
	$: hours = doubleDigit((millisecondsLeft % DAY) / HOUR);
	$: minutes = doubleDigit((millisecondsLeft % HOUR) / MINUTE);
	$: seconds = doubleDigit((millisecondsLeft % MINUTE) / SECOND);

	onMount(() => {
		const interval = setInterval(() => {
			millisecondsLeft = WEDDING_DAY_MILLISECONDS - +new Date();
		}, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<div class="counter">
	<div class="header">DÍAS</div>
	<div />
	<div class="header">HORAS</div>
	<div />
	<div class="header">MINUTOS</div>
	<div />
	<div class="header">SEGUNDOS</div>
	<div class="number">{days}</div>
	<div class="number">:</div>
	<div class="number">{hours}</div>
	<div class="number">:</div>
	<div class="number">{minutes}</div>
	<div class="number">:</div>
	<div class="number">{seconds}</div>
</div>

<style>
	.counter {
		display: grid;
		grid-template-columns: repeat(7, 1fr);
		grid-template-rows: auto auto;
		text-align: center;
		color: rgb(243, 243, 243);
		text-shadow: 8px 8px 8px #b2a9aa;
		margin: 2rem;
	}

	.counter div {
		grid-column: span 1;
		grid-column: span 1;
		padding: 1rem 0;
	}

	.header {
		font-size: 0.8rem;
	}

	.number {
		font-size: 3rem;
	}
</style>
