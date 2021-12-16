<template>
  <header>
    <nav :class="{ 'open' : menuOpen }">
      <ul>
        <li>
          <a href="https://discord/pincer">discord</a>
        </li>
        <li>
          <a href="https://pypi.org/project/Pincer">pypi</a>
        </li>
        <li>
          <a href="https://docs.pincer.dev">documentation</a>
        </li>
        <li>
          <a href="https://github.com/pincer-org/pincer">Github</a>
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
        <svg width="34" height="22" viewBox="0 0 34 22" fill="none" xmlns="http://www.w3.org/2000/svg">
          <g stroke="black" stroke-linejoin="round" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round">
            <path d="M1.41516 1.79492H32.1134"/>
            <path d="M4.91504 11.0708H28.6135"/>
            <path d="M7.61475 20.3467H25.9137"/>
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
        stroke: var(--text-color)
      }

    &.rotated {
      transform: rotate(180deg);
    }

    transition: 0.3s ease-in-out;
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
