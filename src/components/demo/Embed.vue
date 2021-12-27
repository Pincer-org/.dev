<template>
  <div class="embed-container">
    <div class="author">
      <line></line>
      <img src="/img/sigma.png" alt="author' profile picture">
    </div>
    <div class="sender">
        <img src="/icon.svg" alt="Pincer logo">
        <h1>Pincer-Bot <span class="badge">bot</span></h1>
        <p>Today at 12:00 PM</p>
    </div>
    <div class="embed">
      <p><span class="ping">@Sigmanificient</span> said:</p>
      <p><span class="block">Hello, World!</span></p>
    </div>
  </div>
</template>
<style scoped>
  .embed-container {
    background: #363D4E;
    border-radius: 6px;

    display: flex;
    align-items: center;
    justify-content: flex-start;
    padding: 1rem;
    gap: 1rem;

  }
</style>
<script>
  export default {
    name: 'Embed'
  }
</script>