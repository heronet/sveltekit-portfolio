<div class="container">
	<div class="content">
		<p>© 2023 Sirat. All rights reserved.</p>
		<div class="power">
			<span>Powerd by SvelteKit </span>
			<img src="/icons/Svelte.svg" alt="svelte-logo" />
		</div>
	</div>
</div>

<style>
	.container {
		background-color: #000000;
		color: #ffffff;
		padding: 5px 0;
	}
	.content {
		display: flex;
		flex-direction: column;
		max-width: 1366px;
		margin: 20px auto;
		align-items: center;
		justify-content: center;
		padding: 0 20px;
		gap: 10px;
		text-align: center;
	}
	.content > p {
		text-align: center;
		margin: 0;
	}
	.content > .power {
		display: flex;
		align-items: center;
		color: grey;
	}
	.power > img {
		width: 20px;
		height: 20px;
		margin: 0 10px;
	}
	@media (min-width: 768px) {
		.content {
			padding: 0 40px;
		}
	}
</style>
