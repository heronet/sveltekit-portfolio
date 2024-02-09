<div class="container" id="about">
	<div class="content">
		<h1>About me</h1>
		<div>
			<p>
				I'm a software engineer over at Hackules Inc., and let me tell you, my journey into this
				world has been quite the ride. Starting out as a hobbyist, tinkering away with code just for
				fun, I never imagined it would turn into a full-blown passion and profession. But here I am,
				living and breathing all things software.
			</p>
			<p>
				But you know what's really cool? On top of all the coding craziness, I'm also pursuing a
				degree in physics at Shahjalal University of Science and Technology. Yeah, I know, it sounds
				like a handful, but hey, who said you can't have the best of both worlds?
			</p>
			<p>
				It's this blend of technology and science that gets me going every day. Whether I'm deep in
				lines of code or wrapping my head around the mysteries of the universe, I'm constantly
				learning and growing. And let me tell you, there's nothing quite like that feeling of making
				meaningful connections between these two fascinating realms.
			</p>
		</div>
		<div>
			<h2>Education</h2>
			<div class="item">
				<img src="/imgs/SUST.png" alt="" />
				<div class="info">
					<h3>Shahjalal University of Science and Technology</h3>
					<h5>Bachelor of Science - BS, Physics</h5>
					<h6>Jul 2023 - Jan 2027</h6>
				</div>
			</div>
		</div>
		<div>
			<h2>Experience</h2>
			<div class="item">
				<img src="/imgs/HLogo.png" alt="" />
				<div class="info">
					<h3>Software Engineer Intern</h3>
					<h5>Hackules Inc. · Part-timeHackules</h5>
					<h6>Jan 2024 - Present</h6>
					<h6>Wilmington, Delaware, United States · Remote</h6>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		flex-direction: column;
		padding-block: 20px;
	}

	.content {
		padding: 20px;
		max-width: 1366px;
		display: flex;
		flex-direction: column;
		gap: 12px;
		margin-bottom: 20px;
	}
	.content > h1 {
		margin: 12px 0 0 0;
	}
	.item {
		display: flex;
		gap: 12px;
	}
	.item > img {
		max-width: 50px;
		object-fit: contain;
	}
	.item > .info > * {
		margin: 0;
	}

	@media (min-width: 768px) {
		.content {
			padding: 0 40px;
			align-items: start;
			width: fit-content;
		}
		.item {
			align-items: center;
		}
	}

	@media (max-width: 600px) {
		.content {
			text-align: center;
			margin-inline: auto;
		}
		.item {
			flex-direction: column;
			align-items: center;
		}
	}
</style>
