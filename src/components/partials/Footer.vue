<template>
  <footer class="footer">
    <p>Copyright &copy; 2021 - Pincer-org</p>
    <p>Site made by Sigmanificient</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss">
.footer {
  display: flex;
  background-color: var(--bg-color-secondary);
  justify-content: center;
  align-items: center;
  flex-flow: column wrap;
  padding: 1rem;
  gap: 1em;

  p {
    margin: 0;
  }
}
</style>
