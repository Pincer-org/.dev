<script>
export default {
  props: {
    href: {
      type: String,
      default: '#'
    },
    badgeUrl: {
      type: String,
      default: ''
    },
    alt: {
      type: String,
      default: ''
    }
  }
}
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
