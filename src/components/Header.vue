<template>
  <header>
    <div class="left">
      <a href="/" class="logo">
        <img alt="Pincer logo" src="icon.png" width="40px"/>
        Pincer
      </a>
    </div>
    <a id="hamburger" class="hamburger">
      <svg width="34" height="22" viewBox="0 0 34 22" fill="none" xmlns="http://www.w3.org/2000/svg">
        <g stroke="black" stroke-linejoin="round" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round">
          <path d="M1.41516 1.79492H32.1134"/>
          <path d="M4.91504 11.0708H28.6135"/>
          <path d="M7.61475 20.3467H25.9137"/>
        </g>
      </svg>
    </a>
    <nav>
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
  </header>
</template>

<style lang="scss" scoped>
header {
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

  &.hamburger svg g {
    stroke: var(--text-color)
  }

  font-weight: 500;
  font-size: 1.5rem;
}

nav {
  background-color: var(--header-background-color-secondary);
  position: absolute;
  top: 80px;
  width: 100%;
  left: 0;
}

nav ul {
  margin: 40px 0;
  display: flex;
  flex-direction: column;
  gap: 20px;
  justify-content: center;
}

nav li {
  list-style: none;
}
</style>