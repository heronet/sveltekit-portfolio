<script lang="ts">
	import CloseButton from '$lib/ui/CloseButton.svelte';
	import MenuButton from '$lib/ui/MenuButton.svelte';

	const links = [
		{ id: 1, title: 'Skills', url: '#skills' },
		{ id: 2, title: 'Projects', url: '#projects' },
		{ id: 3, title: 'About', url: '#about' }
	];
	let open = false;
	let setOpen = () => {
		open = !open;
	};
</script>

<div class="container">
	<div class="links-container">
		<a href="/" class="brand">
			Sirat<span class="xyz">.site</span>
		</a>
		<ul class="links">
			{#each links as link}
				<li class="link">
					<a href={link.url}>{link.title}</a>
				</li>
			{/each}

			<li>
				<button on:click={setOpen} aria-label="close" class="menu">
					{#if open}
						<CloseButton />
					{:else}
						<MenuButton />
					{/if}
				</button>
			</li>
		</ul>
		{#if open}
			<ul class="dropdown">
				{#each links as link}
					<li class="dropitem">
						<a href={link.url} on:click={setOpen}>
							{link.title}
						</a>
					</li>
				{/each}
			</ul>
		{/if}
	</div>
</div>

<style>
	.container {
		background-color: black;
		color: white;
		width: 100%;
		position: sticky;
		top: 0;
		& .links-container {
			display: flex;
			justify-content: space-between;
			align-items: center;
			max-width: 1366px;
			margin: 0 auto;
			padding: 0 20px;
			position: relative;
			& .brand {
				font-size: 1.5rem;
				color: royalblue;
				font-weight: 600;
				text-transform: uppercase;
				& .xyz {
					color: white;
				}
			}
			& .links {
				padding: 5px 0;
				list-style: none;
				display: flex;
				gap: 15px;
				color: silver;
				& .link {
					cursor: pointer;
				}
				& .link:hover {
					color: white;
				}
				& .menu {
					display: none;
					color: white;
					width: 20px;
					height: 20px;
					background: transparent;
					border: none;
					padding: 0;
				}
			}
			& .dropdown {
				list-style: none;
				background-color: black;
				border-radius: 5px;
				padding: 0;
				position: absolute;
				right: 10px;
				top: 50px;
				& .dropitem {
					padding: 10px;
				}
			}
		}
		@media (min-width: 768px) {
			& .links-container {
				padding: 0 40px;
			}
		}
		@media (max-width: 600px) {
			& .links-container {
				padding: 0 15px;
				& .brand {
					font-size: 1.2rem;
				}
				& .links {
					gap: 0px;
					& .link {
						display: none;
					}
					& .menu {
						display: block;
					}
				}
			}
		}
	}
</style>
