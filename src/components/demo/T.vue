<template>
  <span v-bind:class=c>
    <slot></slot>
  </span>
</template>

<script>
export default {
	props: {
		c: {
			type: String
		}
	}
}
</script>

<style lang="scss">
span {
	&.p {
		color: #B5AAFE
	}

	&.y {
		color: #FEDA8C
	}

	&.b {
		color: #6FAFFE
	}

	&.r {
		color: #FF757F
	}

	&.g {
		color: #78EBB7
	}

	&.k {
		color: #F2C1FE
	}
}
</style>
