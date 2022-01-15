<template>
	<div class="hero">
		<div class="left">
			<h1>Welcome to Pincer!</h1>

			<div class="github-buttons">
				<GhButton
						href="https://pypi.org/project/Pincer"
						badge-url="https://img.shields.io/badge/dynamic/json?label=downloads&query=%24.total_downloads&url=https%3A%2F%2Fapi.pepy.tech%2Fapi%2Fprojects%2FPincer"
						alt="PyPI - Downloads"
				/>
				<GhButton
						href="https://pypi.org/project/Pincer"
						badge-url="https://img.shields.io/pypi/v/Pincer"
						alt="PyPI"
				/>
				<GhButton
						href="https://pypi.org/project/Pincer"
						badge-url="https://img.shields.io/pypi/pyversions/Pincer"
						alt="PyPI - Python Version"
				/>
				<GhButton
						href="https://scrutinizer-ci.com/g/Pincer-org/pincer/?branch=main"
						badge-url="https://scrutinizer-ci.com/g/Pincer-org/pincer/badges/quality-score.png?b=main"
						alt="Scrutinizer Code Quality"
				/>
				<GhButton
						href="https://scrutinizer-ci.com/g/Pincer-org/Pincer/build-status/main"
						badge-url="https://scrutinizer-ci.com/g/Pincer-org/Pincer/badges/build.png?b=main"
						alt="Build Status"
				/>
				<GhButton
						href="https://pincer.readthedocs.io/en/latest/?badge=latest"
						badge-url="https://readthedocs.org/projects/pincer/badge/?version=latest"
						alt="Documentation Status"
				/>
				<GhButton
						href="https://codecov.io/gh/Pincer-org/Pincer"
						badge-url="https://codecov.io/gh/Pincer-org/Pincer/branch/main/graph/badge.svg?token=T15T34KOQW"
						alt="codecov"
				/>
				<GhButton
						href="/"
						badge-url="https://tokei.rs/b1/github/pincer-org/pincer?category=code&path=pincer"
						alt="Lines of code"
				/>
				<GhButton
						href="/"
						badge-url="https://img.shields.io/github/repo-size/Pincer-org/Pincer"
						alt="Repo Size"
				/>
				<GhButton
						href="/"
						badge-url="https://img.shields.io/github/last-commit/Pincer-org/Pincer"
						alt="GitHub last commit"
				/>
				<GhButton
						href="/"
						badge-url="https://img.shields.io/github/commit-activity/m/Pincer-org/Pincer?label=commits"
						alt="GitHub commit activity"
				/>
				<GhButton
						href="/"
						badge-url="https://img.shields.io/github/license/Pincer-org/Pince"
						alt="GitHub"
				/>
				<GhButton
						href="https://discord.gg/pince"
						badge-url="https://img.shields.io/discord/881531065859190804"
						alt="Discord"
				/>
				<GhButton
						href="https://github.com/psf/black"
						badge-url="https://img.shields.io/badge/code%20style-black-000000.svg"
						alt="Code style: black"
				/>
			</div>

			<p>
				🚀 The snappy asynchronous discord api wrapper API wrapper written with aiohttp & websockets for anyone in the
				Python community to build their bot with.
			</p>
			<BlueButton text="Learn more" link="/a"/>

			<h2>Want to explore Pincer?</h2>

			<nav>
				<ul>
					<li>
						<img src="@/assets/icons/github.svg" alt="Github"/>
						<a href="https://github.com/pincer-org/pincer">Take o look at the GitHub repository</a>
					</li>
					<li>
						<img src="@/assets/icons/discord.svg" alt="Discord"/>
						<a href="https://discord/pincer">Join our Discord community</a>
					</li>
					<li>
						<img src="@/assets/icons/pypi.svg" alt="PyPI">
						<a href="https://pypi.org/project/Pincer">Download the PyPI package</a>
					</li>
					<li>
						<img src="@/assets/icons/read_the_docs.svg" alt="ReadTheDocs">
						<a href="https://docs.pincer.dev">Get Started with the documentation</a>
					</li>
				</ul>
			</nav>
		</div>
		<div class="right">
			<BlockCode/>
			<Command/>
			<Embed/>
		</div>
	</div>
</template>

<script>
import BlueButton from '../buttons/BlueButton.vue'
import GhButton from '../buttons/GhButton.vue'

import BlockCode from '../demo/BlockCode.vue'
import Command from "../demo/Command.vue";
import Embed from "../demo/Embed.vue";

export default {
	components: {
		BlueButton,
		GhButton,
		BlockCode,
		Command,
		Embed
	}
}
</script>

<style lang="scss" scoped>
h1 {
	font-size: 1.75rem;
}

h2, p {
	margin-top: 2rem;
}

p {
	text-align: justify;
}

.github-buttons {
	display: flex;
	flex-flow: row wrap;
	gap: 10px;
}

ul {
	li {
		img {
			width: 24px;
			height: 24px;
			filter: invert(1);
		}

		gap: 10px;
		display: flex;
		align-items: center;
		list-style: none;
		margin: 10px 0;

		&:hover, a:focus {
			outline: 0;
			text-decoration: underline;
		}
	}

	padding-left: 0;
	display: grid;
	gap: 5px;
}

.right {
	display: grid;
	gap: 20px;

	img {
		width: calc(100vw - 40px);
	}
}
</style>