<div class="container" id="about">
	<div class="content">
		<h1>About me</h1>
		<div>
			<p>
				Hey there! 👋 I'm a software engineer intern at Hackules Inc., where I get to indulge in my
				passion for coding and tech every day. From tinkering with code as a hobby to now living and
				breathing software development as a profession, it's been quite the journey!
			</p>
			<p>
				But wait, there's more! I'm also studying Physics at Shahjalal University of Science and
				Technology. Balancing both worlds might sound like a handful, but I thrive on the challenge.
				Whether I'm debugging code or diving into the mysteries of the universe, I'm constantly
				driven by curiosity and the quest for knowledge. Let's connect and geek out together! 🚀
			</p>
		</div>
		<div class="list">
			<div>
				<h2>Experience</h2>
				<div class="item">
					<img src="/imgs/HLogo.png" alt="" />
					<div class="info">
						<h3>Software Engineer Intern</h3>
						<h5>Hackules Inc. · Part-time</h5>
						<h6>Jan 2024 - Present</h6>
						<h6>Wilmington, Delaware, United States · Remote</h6>
					</div>
				</div>
			</div>
			<div>
				<h2>Education</h2>
				<div class="item">
					<img src="/imgs/SUST.png" alt="" />
					<div class="info">
						<h3>Shahjalal University of Science and Technology</h3>
						<h5>Bachelor of Science - BS, Physics</h5>
						<h6>Jul 2023 - Jan 2027</h6>
						<h6>Sylhet, Bangladesh</h6>
					</div>
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
		margin-inline: auto;
	}

	.content {
		padding: 20px;
		max-width: 1366px;
		display: flex;
		flex-direction: column;
		gap: 12px;
		margin-bottom: 20px;
		margin-inline: auto;
	}
	.content > h1 {
		margin: 12px 0 0 0;
	}
	.item {
		display: flex;
		gap: 12px;
	}
	.item > img {
		max-width: 70px;
		object-fit: contain;
	}
	.item > .info > * {
		margin: 0;
	}
	.list {
		display: flex;
		flex-direction: column;
		gap: 30px;
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
