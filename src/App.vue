<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Pincer from "./components/Pincer.vue";
import Team from "./components/Team.vue";
import Related from "./components/Related.vue";
import Footer from "./components/Footer.vue";
</script>

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
  padding: 0 20px;
}
</style>