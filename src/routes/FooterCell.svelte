<div class="item">
	<div class="cell">
		<slot />
	</div>
</div>

<style>
	.item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		border-top: 1px solid;
	}

	@media (min-width: 720px) {
		.item {
			flex: 1;
			border-top: none;
			justify-content: flex-start;
		}
	}

	.cell {
		display: flex;
		flex-direction: column;
		padding: 1rem;
	}
</style>
