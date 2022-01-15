<template>
	<header>
		<nav :class="{ 'open' : menuOpen }">
			<ul>
				<li>
					<a href="https://discord/pincer">Discord</a>
				</li>
				<li>
					<a href="https://pypi.org/project/Pincer">PyPI</a>
				</li>
				<li>
					<a href="https://docs.pincer.dev">Documentation</a>
				</li>
				<li>
					<a href="https://github.com/pincer-org/pincer">GitHub</a>
				</li>
			</ul>
		</nav>
		<div class="mobile-header">
			<div class="left">
				<a href="/" class="logo">
					<div class="spin-container">
						<img alt="logo" src="@/assets/logo/icon.svg" width="40"/>
					</div>
					Pincer
				</a>
			</div>
			<a id="hamburger" class="hamburger" @click="toggleMenu()" :class="{ 'rotated' : menuOpen }">
				<svg width="32" height="27" viewBox="0 0 32 27" fill="none" xmlns="http://www.w3.org/2000/svg">
					<g fill="black">
						<path d="M0 0H32V3H0V0Z"/>
						<path d="M0 12H32V15H0V12Z"/>
						<path d="M0 24H32V27H0V24Z"/>
					</g>
				</svg>
			</a>
		</div>
	</header>
</template>

<script>
export default {
	data() {
		return {
			menuOpen: false
		}
	},
	methods: {
		toggleMenu() {
			this.menuOpen = !this.menuOpen
		}
	}
}
</script>

<style lang="scss" scoped>
@keyframes spinFade {
	0% {
		opacity: 0;
		transform: rotate(-360deg);
	}
}

@keyframes Giggle {
	0% {
		transform: rotate(0deg);
	}
	50% {
		transform: rotate(5deg);
	}
	100% {
		transform: rotate(0deg);
	}
}

.mobile-header {
	position: relative;
	background-color: var(--bg-color-secondary);
	height: 80px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 0 20px;
}

.spin-container {
	animation: spinFade 1s cubic-bezier(.35, -0.21, .04, 1.52);
	display: flex;
}

a {
	&.logo {
		display: flex;
		align-items: center;
		gap: 20px;

		&:hover img, &:focus img {
			animation: Giggle 1s cubic-bezier(.35, -0.21, .04, 1.52) infinite;
		}

		&:focus {
			text-decoration: underline;
			outline: none;
		}
	}

	&.hamburger {
		cursor: pointer;

		svg g {
			transition: all 0.3s ease;
			fill: var(--text-color);

			path {
				transition: all 0.3s ease;

				&:nth-child(3) {
					transform-origin: bottom left;
				}
			}
		}

		&.rotated {
			svg g {
				transform: translateX(3px);

				path {
					&:nth-child(1) {
						transform: rotate(45deg);
					}

					&:nth-child(2) {
						transform: scaleX(0)
					}

					&:nth-child(3) {
						transform: rotate(-45deg) translateY(-1.5px) translateX(0.5px);
					}
				}
			}
		}

		transition: 0.3s ease-in-out;
		display: flex;
	}

	font-weight: 500;
	font-size: 1.5rem;
}

nav {
	top: 80px;
	background-color: var(--bg-color-ternary);
	position: absolute;
	width: 100%;
	left: 0;
	transform: translateY(-100%);
	transition: transform 0.3s ease-in-out;
	overflow-x: hidden;

	&.open, &:focus-within {
		transform: translateY(0);
	}

	ul {
		margin: 40px 0;
		display: flex;
		flex-direction: column;
		gap: 20px;
		justify-content: center;
	}

	li {
		list-style: none;
		position: relative;

		&::after {
			content: '';
			position: absolute;
			bottom: 0;
			left: 0;
			width: 0;
			transition: all 0.3s ease-in-out;
			background-color: var(--text-color-secondary);
			height: 2px;
		}

		&:hover, a:focus {
			outline: none;
			color: var(--text-color-secondary);

			&::after {
				width: 10%;
			}
		}
	}
}
</style>
