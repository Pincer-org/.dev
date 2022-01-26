<template>
  <span v-bind:class="c">
    <slot></slot>
  </span>
</template>

<script>
export default {
  props: {
    c: {
      type: String,
    },
  },
};
</script>

<style lang="scss">
span {
  &.p {
    color: #b5aafe;
  }

  &.y {
    color: #feda8c;
  }

  &.b {
    color: #6faffe;
  }

  &.r {
    color: #ff757f;
  }

  &.g {
    color: #78ebb7;
  }

  &.k {
    color: #f2c1fe;
  }
}
</style>
