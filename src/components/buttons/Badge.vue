<template>
	<a class="github-badge" :href="href" tabindex="-1">
		<img :src="badgeUrl" :alt="alt" />
	</a>
</template>

<script>
export default {
	props: {
		href: {
			type: String,
			default: "#",
		},
		badgeUrl: {
			type: String,
			default: "",
		},
		alt: {
			type: String,
			default: "",
		},
	},
};
</script>

<style>
.github-badge {
	user-select: none;
}
</style>
