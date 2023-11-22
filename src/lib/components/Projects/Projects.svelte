<script lang="ts">
	import type { ProjectType } from '$lib/models/project';
	import Project from './Project/Project.svelte';

	const projects: ProjectType[] = [
		{
			id: 1,
			title: 'Connect',
			subtitle: 'A Full-stack social media platform',
			techs: [
				{ id: 1, title: 'Angular', logo: 'Angular' },
				{ id: 2, title: 'ASP.NET Core', logo: 'ASP.NET Core' },
				{ id: 3, title: 'PostgreSQL', logo: 'PostgreSQL' },
				{ id: 4, title: 'TypeScript', logo: 'TypeScript' },
				{ id: 5, title: 'C#', logo: 'C Sharp' },
				{ id: 6, title: 'SASS', logo: 'SASS' },
				{ id: 7, title: 'Docker', logo: 'Docker' },
				{ id: 8, title: 'Google Cloud', logo: 'Google Cloud' }
			],
			links: [
				{ id: 1, title: 'Source', url: 'https://github.com/heronet/connectui' },
				{ id: 2, title: 'Live', url: 'https://uconnect.life/' }
			],
			imgUrl: '/imgs/connect.jpg',
			description:
				'A full-stack social media application that supports real-time chat, posts, comments, photo uploads and user authentication using JWT.'
		},
		{
			id: 2,
			title: 'Shakespeare AI',
			subtitle: 'A Shakespeare simulator backed by OpenAI',
			techs: [
				{ id: 1, title: 'NextJS', logo: 'NextJS alt' },
				{ id: 2, title: 'TailwindCSS', logo: 'Tailwind' },
				{ id: 3, title: 'Shadcn UI', logo: 'ShadcnUI' },
				{ id: 4, title: 'Vercel AI SDK', logo: 'Vercel alt' },
				{ id: 5, title: 'GPT 3.5 Turbo', logo: 'ChatGPT' },
				{ id: 6, title: 'TypeScript', logo: 'TypeScript' }
			],
			links: [
				{ id: 1, title: 'Source', url: 'https://github.com/heronet/ai-chat' },
				{ id: 2, title: 'Live', url: 'https://skpr.online/' }
			],
			imgUrl: '/imgs/SKPR.png',
			description: 'Built with NextJS, OpenAI and Vercel AI SDK, it simulates Shakespeare.'
		},
		{
			id: 3,
			title: 'Journey',
			subtitle: 'A Full-stack hotel booking website',
			techs: [
				{ id: 1, title: 'Angular', logo: 'Angular' },
				{ id: 2, title: 'ASP.NET Core', logo: 'ASP.NET Core' },
				{ id: 3, title: 'PostgreSQL', logo: 'PostgreSQL' },
				{ id: 4, title: 'TypeScript', logo: 'TypeScript' },
				{ id: 5, title: 'C#', logo: 'C Sharp' },
				{ id: 6, title: 'SASS', logo: 'SASS' },
				{ id: 7, title: 'Docker', logo: 'Docker' },
				{ id: 8, title: 'Google Cloud', logo: 'Google Cloud' }
			],
			links: [
				{ id: 1, title: 'Source', url: 'https://github.com/heronet/journey' },
				{ id: 2, title: 'Live', url: 'https://journey-si.web.app' }
			],
			imgUrl: '/imgs/journey.jpg',
			description:
				'A full-stack hotel booking application with user authentication. It supports hotels listing by moderators with photo uploads.'
		},
		{
			id: 4,
			title: 'Sellnet',
			subtitle: 'A Full-stack E-commerce platform',
			techs: [
				{ id: 1, title: 'Angular', logo: 'Angular' },
				{ id: 2, title: 'ASP.NET Core', logo: 'ASP.NET Core' },
				{ id: 3, title: 'PostgreSQL', logo: 'PostgreSQL' },
				{ id: 4, title: 'TypeScript', logo: 'TypeScript' },
				{ id: 5, title: 'C#', logo: 'C Sharp' },
				{ id: 6, title: 'SASS', logo: 'SASS' },
				{ id: 7, title: 'Docker', logo: 'Docker' },
				{ id: 8, title: 'Google Cloud', logo: 'Google Cloud' }
			],
			links: [
				{ id: 1, title: 'Source', url: 'https://github.com/heronet/sellnet' },
				{ id: 2, title: 'Live', url: 'https://sellnet-si.web.app' },
				{
					id: 3,
					title: 'Google Play',
					url: 'https://play.google.com/store/apps/details?id=com.heronet.sellnetbeta&hl=en&gl=US'
				}
			],
			imgUrl: '/imgs/sellnet.jpg',
			description:
				'A full-stack E-commerce application with user authentication. It supports product listing with photo uploads. Also availabe on Android.'
		},
		{
			id: 5,
			title: 'MCQ',
			subtitle: 'A Full-stack MCQ Exam platform',
			techs: [
				{ id: 1, title: 'Angular', logo: 'Angular' },
				{ id: 2, title: 'ASP.NET Core', logo: 'ASP.NET Core' },
				{ id: 3, title: 'PostgreSQL', logo: 'PostgreSQL' },
				{ id: 4, title: 'TypeScript', logo: 'TypeScript' },
				{ id: 5, title: 'C#', logo: 'C Sharp' },
				{ id: 6, title: 'SASS', logo: 'SASS' },
				{ id: 7, title: 'Docker', logo: 'Docker' },
				{ id: 8, title: 'Google Cloud', logo: 'Google Cloud' }
			],
			links: [
				{ id: 1, title: 'Source', url: 'https://github.com/heronet/ksx' },
				{ id: 2, title: 'Live', url: 'https://mcq-si.web.app' }
			],
			imgUrl: '/imgs/mcq.jpg',
			description:
				"A full-stack 'Multiple Choice Questions' exam platform. It supports adding questions by users with advanced features like MathJax."
		}
	];
</script>

<div class="container" id="projects">
	<div class="content">
		<h1>My Works</h1>
		<div class="projects">
			{#each projects as project}
				<Project {project} />
			{/each}
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		background: black;
		color: white;
		scroll-margin-top: 2rem;
	}
	.content {
		max-width: 1366px;
		margin: 0 auto;
		padding: 10px 20px;
	}
	.projects {
		display: flex;
		flex-direction: column;
		gap: 30px;
	}
	@media (max-width: 600px) {
		.content {
			text-align: center;
		}
	}
	@media (min-width: 768px) {
		.content {
			padding: 10px 40px;
		}
	}
</style>
