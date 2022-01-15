<template>
	<div class="command">
		<div class="up">
			<img src="icon.svg" alt="Pincer logo">
			<header>
				<h1>/say <span class="block">message</span></h1>
				<p>Send a custom message!</p>
			</header>
		</div>
		<div class="down">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<circle cx="12" cy="12" r="12" fill="#C4C4C4"/>
				<rect x="5" y="10.5" width="14" height="3" fill="#40444B"/>
				<rect x="10.5" y="19" width="14" height="3" transform="rotate(-90 10.5 19)" fill="#40444B"/>
			</svg>
			<p>/say <span class="block">message: Hello, World!</span></p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Command'
}
</script>

<style lang="scss" scoped>
.command {
	font-size: .75em;
}

.up, .down {
	display: flex;
	align-items: center;
	justify-content: flex-start;
	padding: 1rem;
	gap: 1rem;

	h1, p {
		font-size: 1.25em;
		font-weight: 500;
		margin: 0;
	}

	h1 {
		display: flex;
		align-items: center;
		margin-bottom: 4px;
		gap: 4px
	}

	img {
		height: 1.5rem;
	}
}

.up {
	background-color: var(--header-background-color);
	border-top-left-radius: .5em;
	border-top-right-radius: .5em;
}

.down {
	background-color: var(--discord-lighter-color);
	border-bottom-left-radius: .5em;
	border-bottom-right-radius: .5em;
}

span.block {
	font-size: .75em;
	background: var(--discord-darker-color);
	padding: .2rem .4rem;
	border-radius: .25rem;
	color: var(--text-color-secondary);
}
</style>
