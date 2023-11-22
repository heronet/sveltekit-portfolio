<script lang="ts">
	import TechItem from '$lib/ui/TechItem.svelte';

	export let category: string;
	export let items: { id: number; title: string; logo: string }[];
</script>

<div class="container">
	<h2 class="name">{category}</h2>
	<ul class="list">
		{#each items as skill}
			<TechItem tech={skill} />
		{/each}
	</ul>
</div>

<style>
	.list {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	@media (max-width: 600px) {
		.container {
			display: flex;
			flex-direction: column;
			align-items: center;
		}
		.list {
			flex-wrap: wrap;
			flex-direction: row;
			justify-content: center;
			gap: 20px;
			margin-top: 0;
		}
	}
</style>
