<template>
	<div class="embed-container">
		<div class="author">
			<svg viewBox="0 0 28 10" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path
					d="M27.3652 1.78945L6.04371 1.78945C3.28228 1.78945 1.04371 4.02802 1.04371 6.78945V9.75293"
					stroke="#4F545C"
					stroke-width="2"
				/>
			</svg>

			<img src="@/assets/members/Sigma.png" alt="author' profile picture" />
			<p class="name">Sigmanificient</p>
			<p class="command-used">used <span class="block">/say</span></p>
		</div>
		<div class="sender">
			<img src="@/assets/logo/icon.svg" alt="Pincer logo" />
			<h1>Pincer-Bot <span class="block badge">bot</span></h1>
			<p>Today at 12:00 PM</p>
		</div>
		<div class="embed">
			<p><span class="block ping">@Sigmanificient</span> said:</p>
			<p><span class="block block-code">Hello, World!</span></p>
		</div>
	</div>
</template>

<script>
export default {
	name: "Embed",
};
</script>

<style lang="scss" scoped>
.embed-container {
	font-size: 0.75em;
	background: var(--discord-color-lighter);
	border-radius: 6px;
	display: grid;
	padding: 1rem 1rem 2rem;
}

.author {
	margin-left: 15px;
	display: flex;
	align-items: center;
	gap: 0.5em;

	p {
		font-size: 0.75em;
		margin: 0;
	}

	svg {
		margin-top: 0.25rem;
		margin-bottom: 0.2rem;
		width: 32px;
	}

	img {
		height: 0.8em;
		width: 0.8em;
	}
}

.name {
	font-size: 0.75em;
	font-weight: bold;
}

.command-used {
	color: var(--text-color-secondary);

	span {
		padding: 0;
		font-weight: bold;
		color: var(--button-color);
	}
}

.sender {
	display: flex;
	align-items: center;
	gap: 0.5em;
	height: 2em;

	h1 {
		margin: 0;
		font-size: 0.8em;
		font-weight: 500;
	}

	p {
		font-size: 0.75em;
		color: var(--text-color-secondary);
	}

	img {
		margin-left: 0.2em;
		margin-right: 0.5em;
		height: 2em;
		width: 2em;
	}
}

.embed {
	margin-left: 3em;
	background-color: var(--bg-color-secondary);
	padding: 0.6em 1em;
	border-radius: 0.4em;
	border-left: 0.4em solid var(--button-color);
	width: max-content;
}

.block {
	padding: 0.1rem 0.3rem;
	border-radius: 0.25rem;
	color: var(--text-color-secondary);

	&-code {
		background: var(--discord-color-darker);
	}

	&.ping {
		background-color: var(--discord-ping-color);
	}

	&.badge {
		background-color: var(--discord-badge-color);
		color: var(--text-color);
		text-transform: uppercase;
		font-size: 0.75em;
		margin-left: 0.5em;
	}
}

@media screen and (min-width: 979px) {
	.embed {
		margin-left: 6em;
		display: inline-block;
		font-size: 0.6em;
		gap: 0;
	}

	.sender img {
		width: 1rem;
		margin-inline: 1em 0.5em;
	}
}

@media screen and (min-width: 980px) {
	.embed-container {
		margin-left: 12em;
		width: 60%;
		animation: slideInTopFade 1s ease forwards;
		animation-delay: 1s;
		opacity: 0;
	}
}
</style>
