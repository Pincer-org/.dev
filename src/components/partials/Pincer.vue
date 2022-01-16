<template>
	<div id="more" class="about">
		<h2>Pincer, the discord lib from scratch.</h2>
		<p>
			After the announcement of discord.py dropping maintenance, we took the decision to build a new API wrapper, built
			from ground zero. This decision is based on the fact that the current implementation of the old library does not
			allow for a easy integration of slash commands. Indeed, the whole package has been built to use message content as
			the way to create commands, using a bot prefix. Changing the core mechanics of discord.py would require to rewrite
			a
			lot of it. Pincer on the other hand is built to take fully the new integration and slash commands system.
		</p>
		<p>
			The project has also been started by Sigmanificient, a student developer in order to learn more about open-source
			management, Github maintaining and Python. Today, Pincer has been stared over 80 times on Github, and more than 20
			people have contributed to make the package better while the alpha version is still in development!
		</p>
		<div class="details">
			<div class="left">
				<h3>You can make the change</h3>
				<p>
					Participating in the collaboration of Pincer is really easy, as our community is welcoming any level of
					developer
					and always ready to help you! We are not just building an API wrapper, we are creating the library you want to
					use. Tired of having everything to change across all your bots? Join our contributors by Implementing your
					code
					in our project!
				</p>
				<BlueButton text="Start Contributing" link="https://github.com/Pincer-org/issues"/>
			</div>
			<div class="right">
				<h3>We want to make it right</h3>
				<p>
					With Pincer, we are taking the time to write more pythonic code, by following the trending rules of the Python
					programming language. We are using popular tools all across the Python community such as mypy, flake8, black,
					sphinx, pyproject, setup.cfg, pytest and pre-commit to create our dream library with the best developer
					environment.
				</p>
				<BlueButton text="Lib Explanations" link="https://docs.pincer.dev"/>
			</div>
		</div>
	</div>
</template>

<script>

import BlueButton from "@/components/buttons/Btn";

export default {
	name: 'Pincer',
	components: {
		BlueButton
	}
}
</script>

<style lang="scss" scoped>
.about p {
	text-align: justify;
}

.details {
	margin-top: 40px;
	display: flex;
	flex-direction: column;
	gap: 40px;
}

.left {
	position: relative;

	&::before {
		content: '';
		position: absolute;
		inset: 0;

		background: url('../../assets/decorations/pull_request.svg') no-repeat center;
		background-size: 75% 75%;
		z-index: -1;
		opacity: 0.2;
	}
}

.right {
	position: relative;

	&::before {
		content: '';
		position: absolute;
		inset: 0;

		background: url('../../assets/decorations/magnifying-glass.svg') no-repeat center;
		background-size: 75% 75%;
		z-index: -1;
		opacity: 0.2;
	}
}

@media (min-width: 540px) {
	.details {
		flex-direction: row;
	}
}
</style>
