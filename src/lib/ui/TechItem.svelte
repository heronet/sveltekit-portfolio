<script lang="ts">
	export let tech: {
		id: number;
		title: string;
		logo: string;
	};
</script>

<li class="item">
	<img src={`/icons/${tech.logo}.svg`} alt={tech.title} class="img" />
	<span>{tech.title}</span>
</li>

<style>
	.item {
		display: flex;
		gap: 10px;
		align-items: center;
		font-size: 15px;
	}
	.img {
		width: 25px;
	}
	@media (max-width: 600px) {
		.item {
			font-size: small;
		}
		.img {
			width: 25px;
		}
	}
</style>
