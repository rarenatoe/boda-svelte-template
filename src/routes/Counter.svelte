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
	<div class="header">
		<div class="cell"><h5>DÍAS</h5></div>
		<div class="separator"><h1 class="hidden">:</h1></div>
		<div class="cell"><h5>HORAS</h5></div>
		<div class="separator"><h1 class="hidden">:</h1></div>
		<div class="cell"><h5>MINUTOS</h5></div>
		<div class="separator"><h1 class="hidden">:</h1></div>
		<div class="cell"><h5>SEGUNDOS</h5></div>
	</div>
	<div class="number-list number">
		<div class="cell"><h1>{days}</h1></div>
		<div class="separator pad-vertical"><h1>:</h1></div>
		<div class="cell"><h1>{hours}</h1></div>
		<div class="separator"><h1>:</h1></div>
		<div class="cell"><h1>{minutes}</h1></div>
		<div class="separator pad-vertical"><h1>:</h1></div>
		<div class="cell"><h1>{seconds}</h1></div>
	</div>
</div>

<style>
	.counter {
		display: flex;
		flex-direction: column;
		margin: 1rem 0;
	}
	.header {
		display: flex;
		flex-direction: row;
	}
	.number-list {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		border-top: 1px solid rgba(0, 0, 0, 0.1);
		border-bottom: 1px solid rgba(0, 0, 0, 0.1);
	}
	.number {
		font-size: 64px;
	}
	.cell {
		display: flex;
		flex: 1 1 0;
		justify-content: center;
		padding-left: 8px;
		padding-right: 8px;
	}
	.separator {
		display: flex;
		justify-content: center;
	}
	.hidden {
		visibility: hidden;
		margin: 0;
	}
</style>
