<template>
	<Header/>
	<main>
		<Hero/>
		<Pincer/>
		<Team/>
		<Related/>
	</main>
	<Footer/>
</template>

<script>
import Header from "@/components/partials/Header.vue";
import Hero from "@/components/partials/Hero.vue";
import Pincer from "@/components/partials/Pincer.vue";
import Team from "@/components/partials/Team.vue";
import Related from "@/components/partials/Related.vue";
import Footer from "@/components/partials/Footer.vue";

export default {
	name: 'App',
	components: {
		Header,
		Hero,
		Pincer,
		Team,
		Related,
		Footer
	},
}
</script>

<style lang="scss">
:root {
	scroll-behavior: smooth;
	--text-color: #FFFFFF;
	--text-color-secondary: #DCDDEA;

	--bg-color: #222635;
	--bg-color-secondary: #2B3448;
	--bg-color-ternary: #303A4F;

	--discord-color-darker: #191C2B;
	--discord-color-lighter: #363D4E;

	--discord-ping-color: #3B406F;
	--discord-badge-color: #5865F2;

	--button-color: #1475C3;
	--button-shadow-color: #0d5894;
}

::-webkit-scrollbar {
	width: 10px;
	height: 10px;

	&-track {
		background: var(--bg-color);
	}

	&-thumb {
		background: var(--bg-color-secondary);
	}

	&-corner {
		background: var(--bg-color);
	}
}

* {
	/* Firefox scrollbar */
	scrollbar-color: var(--button-color) var(--bg-color);

	&::selection {
		background-color: var(--bg-color-secondary);
		color: var(--text-color-secondary);
	}
}

body {
	margin: 0;
	color: var(--text-color);
	font-size: clamp(12px, 1vw, 24px);
	font-family: 'Poppins', sans-serif;
	font-weight: 500;
	background-color: var(--bg-color);
}

main {
	display: grid;
	gap: 4em;
	width: min(calc(100% - 40px), 1400px);
	padding: 0 20px;
	margin: 0 auto;
}

a {
	color: inherit;
	text-decoration: none;
}

img {
	user-select: none;
}

@keyframes windowClose {
	0% {
		opacity: 1;
	}

	50% {
		transform: scaleY(1);
	}

	100% {
		transform-origin: top right;
		transform: scaleY(0);
		opacity: 0;
	}
}

@keyframes slideInLeftFade {
	0% {
		transform: translateX(-10%);
		opacity: 0;
	}

	100% {
		transform: translateX(0);
		opacity: 1;
	}
}

@keyframes slideInTopFade {
	0% {
		transform: translateY(-5%);
		opacity: 0;
	}

	100% {
		transform: translateY(0);
		opacity: 1;
	}
}
</style>