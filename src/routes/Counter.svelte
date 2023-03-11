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

	const numDays = millisecondsLeft / DAY;
	const numHours = (millisecondsLeft % DAY) / HOUR;

	let stage = 0;
	if (numDays > -1 && numDays < 0 && numHours > -7) stage = 1;
	else if (numDays < 0) {
		stage = 2;
	}

	$: days = doubleDigit(Math.max(numDays, 0));
	$: hours = doubleDigit(Math.max(numHours, 0));
	$: minutes = doubleDigit((Math.max(millisecondsLeft % HOUR) / MINUTE, 0));
	$: seconds = doubleDigit(Math.max((millisecondsLeft % MINUTE) / SECOND, 0));

	onMount(() => {
		const interval = setInterval(() => {
			millisecondsLeft = WEDDING_DAY_MILLISECONDS - +new Date();
		}, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<div class={`counter ${stage === 1 ? 'flash' : ''}`}>
	{#if stage < 2}
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
	{:else}
		<div class="number" style="grid-column: span 7;">¡Gracias por asistir!</div>
	{/if}
</div>

<style>
	.counter {
		display: grid;
		grid-template-columns: repeat(7, 1fr);
		grid-template-rows: auto auto;
		text-align: center;
		color: rgb(243, 243, 243);
		text-shadow: 3px 3px 4px black;
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

	.flash {
		animation-name: flash-animation;
		animation-duration: 1.5s;
		animation-timing-function: linear;
		animation-iteration-count: infinite;
	}

	@keyframes flash-animation {
		0% {
			opacity: 1;
		}
		50% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
</style>
