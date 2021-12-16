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
          <img alt="logo" src="icon.svg" width="40"/>
          Pincer
        </a>
      </div>
      <a id="hamburger" class="hamburger" @click="menuOpen = !menuOpen" :class="{ 'rotated' : menuOpen }">
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

<style lang="scss" scoped>
.mobile-header {
  position: relative;
  background-color: var(--header-background-color);
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
}

a {
  &.logo {
    display: flex;
    align-items: center;
    gap: 20px;
  }

  &.hamburger {
      svg g {
        fill: var(--text-color)
      }

    &.rotated {
      transform: rotate(180deg);
    }

    transition: 0.3s ease-in-out;
    display: flex;
  }

  font-weight: 500;
  font-size: 1.5rem;
}

nav {
  top: 80px;
  background-color: var(--header-background-color-secondary);
  position: absolute;
  width: 100%;
  left: 0;
  transform: translateY(-100%);
  transition: transform 0.3s ease-in-out;

  &.open {
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
  }
}
</style>
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
