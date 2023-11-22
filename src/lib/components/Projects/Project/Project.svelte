<script lang="ts">
	import type { ProjectType } from '$lib/models/project';
	import TechItem from '$lib/ui/TechItem.svelte';

	export let project: ProjectType;
</script>

<div class="container">
	<div class="img-container">
		<img src={project.imgUrl} alt={project.title} class="img" />
	</div>
	<div class="info">
		<h2 class="title">{project.title}</h2>
		<h3 class="subtitle">{project.subtitle}</h3>
		<span>{project.description}</span>
		<ul class="links">
			{#each project.links as link}
				<li>
					<a href={link.url} class="link">
						{link.title}
					</a>
				</li>
			{/each}
		</ul>
		<h3>Tech used</h3>
		<ul class="tech">
			{#each project.techs as item}
				<TechItem tech={item} />
			{/each}
		</ul>
	</div>
</div>

<style>
	.container {
		margin: 40px auto;
		display: flex;
		gap: 40px;
		width: 100%;
		justify-content: space-between;
	}
	.container:nth-child(2n + 1) {
		flex-direction: row-reverse;
	}
	.title {
		margin-top: 0;
		padding-top: 0;
	}
	.subtitle {
		color: royalblue;
	}
	.tech {
		padding: 0;
		display: flex;
		gap: 16px;
		flex-wrap: wrap;
	}
	.img-container {
		flex: 1;
		max-width: 400px;
		height: max-content;
		box-shadow: 8px 10px 133px -7px rgba(65, 105, 225, 0.73);
		-webkit-box-shadow: 8px 10px 133px -7px rgba(65, 105, 225, 0.73);
		-moz-box-shadow: 8px 10px 133px -7px rgba(65, 105, 225, 0.73);
	}
	.info {
		flex: 1;
	}
	.img {
		max-width: 100%;
	}
	.links {
		list-style: none;
		padding: 0;
		display: flex;
		gap: 10px;
		flex-wrap: wrap;

		& .link {
			border: 1px solid royalblue;
			border-radius: 5px;
			padding: 5px 10px;
			color: white;
			display: inline-block;
			transition: all 0.15s ease-in-out;
			font-size: 14px;
			text-transform: uppercase;
		}
		& .link:hover {
			box-shadow:
				0 0 10px 0 royalblue inset,
				0 0 20px 2px royalblue;
			border: 1px solid royalblue;
		}
	}
	@media (max-width: 600px) {
		.container {
			flex-direction: column;
			align-items: center;
		}
		.container:nth-child(2n + 1) {
			flex-direction: column;
		}
		.tech {
			justify-content: center;
		}
		.links {
			justify-content: center;
		}
	}
</style>
