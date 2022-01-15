<template>
	<div id="app">
		<Header/>
		<main>
			<Hero/>
			<Pincer/>
			<Team/>
			<Related/>
		</main>
		<Footer/>
	</div>
</template>

<script>
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import Pincer from "@/components/Pincer.vue";
import Team from "@/components/Team.vue";
import Related from "@/components/Related.vue";
import Footer from "@/components/Footer.vue";

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
// give member their scrollbar scss style
::-webkit-scrollbar {
	width: 10px;
	height: 10px;

	&-track {
		background: var(--main-background-color);
	}

	&-thumb {
		background: var(--header-background-color);
	}

	&-corner {
		background: var(--main-background-color);
	}
}

/* Firefox */
* {
	scrollbar-color: var(--button-color) var(--main-background-color);
}

*::selection {
	background-color: var(--header-background-color);
	color: var(--text-color-secondary);
}

body {
	background-color: var(--main-background-color);
}

main {
	display: grid;
	gap: 2em;
	width: clamp(280px, calc(100% - 40px), 1400px);
	padding: 0 20px;
	margin: 0 auto;
}
</style>