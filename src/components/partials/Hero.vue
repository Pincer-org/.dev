<template>
	<div class="hero">
		<div class="hero-left">
			<div class="landing">
				<h1>Welcome to Pincer!</h1>
				<div class="github-buttons">
					<Badge
							href="https://pypi.org/project/Pincer"
							badge-url="https://img.shields.io/badge/dynamic/json?label=downloads&query=%24.total_downloads&url=https%3A%2F%2Fapi.pepy.tech%2Fapi%2Fprojects%2FPincer"
							alt="PyPI - Downloads"
					/>
					<Badge
							href="https://pypi.org/project/Pincer"
							badge-url="https://img.shields.io/pypi/v/Pincer"
							alt="PyPI"
					/>
					<Badge
							href="https://pypi.org/project/Pincer"
							badge-url="https://img.shields.io/pypi/pyversions/Pincer"
							alt="PyPI - Python Version"
					/>
					<Badge
							href="https://scrutinizer-ci.com/g/Pincer-org/pincer/?branch=main"
							badge-url="https://scrutinizer-ci.com/g/Pincer-org/pincer/badges/quality-score.png?b=main"
							alt="Scrutinizer Code Quality"
					/>
					<Badge
							href="https://scrutinizer-ci.com/g/Pincer-org/Pincer/build-status/main"
							badge-url="https://scrutinizer-ci.com/g/Pincer-org/Pincer/badges/build.png?b=main"
							alt="Build Status"
					/>
					<Badge
							href="https://pincer.readthedocs.io/en/latest/?badge=latest"
							badge-url="https://readthedocs.org/projects/pincer/badge/?version=latest"
							alt="Documentation Status"
					/>
					<Badge
							href="https://codecov.io/gh/Pincer-org/Pincer"
							badge-url="https://codecov.io/gh/Pincer-org/Pincer/branch/main/graph/badge.svg?token=T15T34KOQW"
							alt="codecov"
					/>
					<Badge
							href="/"
							badge-url="https://tokei.rs/b1/github/pincer-org/pincer?category=code&path=pincer"
							alt="Lines of code"
					/>
					<Badge
							href="/"
							badge-url="https://img.shields.io/github/repo-size/Pincer-org/Pincer"
							alt="Repo Size"
					/>
					<Badge
							href="/"
							badge-url="https://img.shields.io/github/last-commit/Pincer-org/Pincer"
							alt="GitHub last commit"
					/>
					<Badge
							href="/"
							badge-url="https://img.shields.io/github/commit-activity/m/Pincer-org/Pincer?label=commits"
							alt="GitHub commit activity"
					/>
					<Badge
							href="/"
							badge-url="https://img.shields.io/github/license/Pincer-org/Pince"
							alt="GitHub"
					/>
					<Badge
							href="https://discord.gg/pince"
							badge-url="https://img.shields.io/discord/881531065859190804"
							alt="Discord"
					/>
					<Badge
							href="https://github.com/psf/black"
							badge-url="https://img.shields.io/badge/code%20style-black-000000.svg"
							alt="Code style: black"
					/>
				</div>

				<p>
					🚀 The snappy asynchronous discord api wrapper API wrapper written with aiohttp & websockets for anyone in the
					Python community to build their bot with.
				</p>
				<Btn text="Learn more" @click="scrollDown()"/>

			</div>

			<div class="explore">
				<h2>Want to explore Pincer?</h2>

				<nav>
					<ul class="explore-container">
						<li class="explore-item">
							<img src="@/assets/icons/github.svg" alt="Github"/>
							<a href="https://github.com/pincer-org/pincer">Take o look at the GitHub repository</a>
						</li>
						<li class="explore-item">
							<img src="@/assets/icons/discord.svg" alt="Discord"/>
							<a href="https://discord/pincer">Join our Discord community</a>
						</li>
						<li class="explore-item">
							<img src="@/assets/icons/pypi.svg" alt="PyPI">
							<a href="https://pypi.org/project/Pincer">Download the PyPI package</a>
						</li>
						<li class="explore-item">
							<img src="@/assets/icons/read_the_docs.svg" alt="ReadTheDocs">
							<a href="https://docs.pincer.dev">Get Started with the documentation</a>
						</li>
					</ul>
				</nav>
			</div>
		</div>
		<div class="hero-right">
			<BlockCode/>
			<img class="arrow arrow-left" src="@/assets/decorations/arrow.svg" alt="...">

			<div class="result">
				<Command/>
				<img class="arrow arrow-right" src="@/assets/decorations/arrow.svg" alt="...">
				<Embed/>
			</div>
		</div>
	</div>
</template>

<script>
import Btn from '../buttons/Btn.vue'
import Badge from '../buttons/Badge.vue'

import BlockCode from '../demo/BlockCode.vue'
import Command from "../demo/Command.vue";
import Embed from "../demo/Embed.vue";

export default {
	components: {
		Btn,
		Badge,
		BlockCode,
		Command,
		Embed
	},
	methods: {
		scrollDown() {
			location.hash = '#more';
		}
	}
}
</script>

<style lang="scss" scoped>
.hero-left {
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.landing {
	h1 {
		font-size: 2rem;
	}

	p {
		margin-top: 2rem;
		text-align: justify;
	}
}

.github-buttons {
	display: flex;
	flex-flow: row wrap;
	gap: 10px;
}

.explore {
	position: relative;

	&-container {
		padding-left: 0;
		display: grid;
		gap: 5px;
	}

	&-item {
		gap: 10px;
		display: flex;
		align-items: center;
		list-style: none;
		margin: 10px 0;

		&:hover, a:focus {
			outline: 0;
			text-decoration: underline;
		}

		img {
			width: 24px;
			height: 24px;
			filter: invert(1);
		}

		h2 {
			margin-top: 2rem;
		}
	}

	&::before {
		content: '';
		position: absolute;
		inset: 0;
		opacity: 0.2;
		background: url('../../assets/decorations/help.svg') no-repeat center;
		background-size: 75% 75%;
		z-index: -1;
	}
}


.hero-right {
	display: grid;
	gap: 40px;

	img {
		width: calc(100vw - 40px);
	}
}

.result {
	display: grid;
	gap: 40px;
}

.arrow {
	display: none;
}

@media screen and (min-width: 720px) and (max-width: 979px) {
	.hero-left {
		gap: 40px;
	}

	.explore {
		min-width: 300px;

		&-container {
			display: flex;
			gap: 20px;
		}
	}

	.hero-right {
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr;
	}
}

@media screen and (min-width: 980px) {
	.hero {
		margin-top: 20px;
		display: flex;
		gap: 64px;

		&-left {
			width: 100%;
			animation: slideInLeftFade 2s ease;
		}

		&-right {
			display: flex;
			flex-direction: column;
			width: 110%;
			gap: 0;
		}
	}

	.result {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 0;
	}

	.arrow {
		display: flex;
		width: 100% !important;
		height: 40px;
		overflow: hidden;

		&-left {
			opacity: 0;
			animation: slideInTopFade 1s ease forwards;
			animation-delay: 1s;
		}

		&-right {
			animation: slideInTopFadeInv 1s ease forwards;
			animation-delay: 1.5s;
			opacity: 0;
		}
	}
}
</style>
