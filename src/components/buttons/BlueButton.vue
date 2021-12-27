<script>
export default {
  props: {
    text: {
      type: String
    },
    link: {
      type: String
    },
  }
}

</script>
<template>
  <a class="btn" v-bind:href=link target="_blank">{{ text }}</a>
</template>
<style lang="scss" scoped>
.btn {
  color: #fff;
  display:inline-block;
  background: var(--button-color);
  border-radius: 6px;
  padding: 1em 2em;

  transition: all 0.1s ease-in-out;
  box-shadow: 0 4px var(--button-shadow-color);
  user-select: none;

  &:focus-within:not(:active) {
    border: 1px solid var(--text-color);
  }

  &:hover {
    transform: translateY(2px);
    box-shadow: 0 2px var(--button-shadow-color);
  }

  &:active {
    background: var(--button-shadow-color);
    transition: all 0.1s ease-in-out;
    transform: translateY(4px);
    box-shadow: none;
  }
}
</style>