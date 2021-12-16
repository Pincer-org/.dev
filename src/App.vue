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
body {
  background-color: var(--main-background-color);
}
</style>
