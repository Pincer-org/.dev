<script setup>
defineProps({href: String, badgeUrl: String, alt: String})
</script>
<template>
  <a v-bind:href=href>
    <img v-bind:src=badgeUrl v-bind:alt=alt>
  </a>
</template>
