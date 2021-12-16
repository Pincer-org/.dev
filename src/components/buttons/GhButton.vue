<script setup>
defineProps({href: String, badgeUrl: String, alt: String})
</script>
<template>
  <a v-bind:href=href tabindex="-1">
    <img v-bind:src=badgeUrl v-bind:alt=alt>
  </a>
</template>
<style scoped>
  a {
    user-select: none;
  }
</style>
