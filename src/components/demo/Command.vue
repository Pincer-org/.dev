<template>
	<div class="command">
		<div class="command-up">
			<img src="@/assets/logo/icon.svg" alt="Pincer logo" />
			<header>
				<h1>/say <span class="block">message</span></h1>
				<p>Send a custom message!</p>
			</header>
		</div>
		<div class="command-down">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<circle cx="12" cy="12" r="12" fill="#C4C4C4" />
				<rect x="5" y="10.5" width="14" height="3" fill="#40444B" />
				<rect x="10.5" y="19" width="14" height="3" transform="rotate(-90 10.5 19)" fill="#40444B" />
			</svg>
			<p>/say <span class="block">message: Hello, World!</span></p>
		</div>
	</div>
</template>

<script>
export default {
	name: "Command",
};
</script>

<style lang="scss" scoped>
.command {
	font-size: 0.5em;

	&-up,
	&-down {
		display: flex;
		align-items: center;
		justify-content: flex-start;
		padding: 0.75rem 0.75rem 0.75rem 1rem;
		gap: 0.75rem;

		p {
			font-size: 1.25em;
			font-weight: 500;
			margin: 0;
		}
	}

	&-up {
		background-color: var(--bg-color-secondary);
		border-top-left-radius: 0.5em;
		border-top-right-radius: 0.5em;

		h1 {
			font-size: 1.25em;
			font-weight: 500;
			display: flex;
			align-items: center;
			margin: 0 0 4px;
			gap: 4px;
		}

		img {
			height: 1.5rem;
		}
	}

	&-down {
		background-color: var(--discord-color-lighter);
		border-bottom-left-radius: 0.5em;
		border-bottom-right-radius: 0.5em;
		padding-left: 3em;
		gap: 1rem;

		svg {
			width: 2em;
		}
	}
}

.block {
	font-size: 0.75em;
	background: var(--discord-color-darker);
	padding: 0.2rem 0.4rem;
	border-radius: 0.25rem;
	color: var(--text-color-secondary);
}

@media screen and (min-width: 980px) {
	.command {
		animation: slideInTopFade 1s ease forwards;
		animation-delay: 0.5s;
		opacity: 0;
		margin-left: 4em;
		width: 60%;
	}
}
</style>
