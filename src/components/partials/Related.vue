<template>
	<div class="related">
		<h2>Related projects</h2>

		<div class="left">
			<h3>The Pincer CLI</h3>
			<p>
				In the intent to simplify pincer user life, we are building a console line interface tools that will bring
				automation to the pincer package. Commands to import templates, create cogs and commands are going to make the
				developer experience easier and straight forward, faster and open to beginners.
			</p>
			<BlueButton text="Github Repository" link="https://github.com/Pincer-org/cli"/>
		</div>
		<div class="right">
			<h3>The Pincer Bot</h3>
			<p>
				Our discord server need a powerful yet fun bot to interact with and demonstrate the key features of our library.
				It will also be a good example for an advanced Bot, running in production, that new users can explore to
				understand how they can use the library and take advantage of it.
			</p>
			<BlueButton text="Github Repository" link="https://github.com/Pincer-org/bot"/>
		</div>
	</div>
</template>

<script>
import BlueButton from '../buttons/BlueButton.vue';

export default {
	name: 'Related',
	components: {
		BlueButton,
	}
}
</script>

<style lang="scss" scoped>
h2, .right {
	margin: 40px 0;
}

p {
	text-align: justify;
}
</style>