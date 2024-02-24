<script lang="ts">
	const socials = [
		{
			id: 1,
			url: 'https://www.linkedin.com/in/siratul-islam/',
			title: 'LinkedIn'
		},
		{ id: 2, url: 'https://github.com/heronet/', title: 'Github' },
		{ id: 3, url: 'https://www.facebook.com/senorsirat/', title: 'Facebook' }
	];
</script>

<div id="hero" class="container">
	<div class="intro">
		<div class="text">
			<div class="title">
				<span class="name"> I'm Sirat</span>, <br />
				<span>A Software Engineer.</span>
			</div>
			<div class="desc">
				I develop Mobile and Full-stack Web applications. I love to make my ideas come to life using
				modern technologies.
			</div>
			<a href="/pdfs/resume.pdf" class="resume"> My Resume </a>
		</div>
		<div class="details">
			<img src="/imgs/me.jpeg" alt="me" class="img" />
			<ul class="social">
				{#each socials as social}
					<li class="item">
						<img src={`/icons/${social.title}.svg`} alt={social.title} class="icon" />
						<a href={social.url}>{social.title}</a>
					</li>
				{/each}
			</ul>
		</div>
	</div>
</div>

<style>
	.container {
		width: 100%;
		background-color: black;
		color: white;
		& .intro {
			max-width: 1366px;
			margin: 0 auto;
			padding: 40px 20px;
			display: flex;
			justify-content: space-between;
			gap: 50px;
			& .text {
				display: flex;
				flex-direction: column;
				& .title {
					font-size: 3rem;
					line-height: 1.3;
					& .name {
						color: royalblue;
					}
				}
				& .desc {
					margin: 10px 0;
					color: silver;
				}
				& .resume {
					display: block;
					background-color: royalblue;
					border: 1px solid royalblue;
					border-radius: 5px;
					margin-top: 10px;
					padding: 7px 12px;
					max-width: fit-content;
					text-transform: uppercase;
					transition: all 0.15s ease-in-out;
				}
				& .resume:hover {
					box-shadow:
						0 0 10px 0 royalblue inset,
						0 0 20px 2px royalblue;
					border: 1px solid royalblue;
				}
			}
			& .details {
				display: flex;
				flex-direction: column;
				align-items: center;
				gap: 25px;
				& .img {
					display: block;
					max-width: 200px;
					border-radius: 50%;
				}
				& .social {
					list-style: none;
					display: flex;
					gap: 15px;
					padding: 0;
					font-size: 0.8rem;
					& .item {
						display: flex;
						flex-direction: column;
						align-items: center;
						gap: 5px;
						cursor: pointer;
						& .icon {
							width: 20px;
						}
					}
					& .item:hover {
						text-decoration: underline;
					}
				}
			}
		}
		@media (min-width: 768px) {
			& .intro {
				padding: 80px 40px 40px 40px;
			}
		}
		@media (max-width: 600px) {
			& .intro {
				flex-direction: column-reverse;
				align-items: center;
				justify-content: center;
				text-align: center;
				gap: 0;
				& .text {
					& .resume {
						margin-inline: auto;
						font-size: 0.9rem;
						padding: 5px 10px;
					}
					& .title {
						font-size: 2.2rem;
					}
					& .desc {
						font-size: 0.9rem;
					}
				}
				& .details {
					gap: 15px;
					& .img {
						max-width: 120px;
					}
					& .social {
						gap: 15px;

						& .item {
							& .icon {
								width: 16px;
							}
						}
					}
				}
			}
		}
	}
</style>
