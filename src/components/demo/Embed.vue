<template>
  <div class="embed-container">
    <div class="author">
      <svg viewBox="0 0 28 10" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M27.3652 1.78945L6.04371 1.78945C3.28228 1.78945 1.04371 4.02802 1.04371 6.78945V9.75293" stroke="#4F545C" stroke-width="2"/>
      </svg>

      <img src="/img/sigma.png" alt="author' profile picture">
      <p class="name">Sigmanificient</p>
      <p class="command-used">used <span>/say</span></p>

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
<style lang="scss" scoped>
  .embed-container {
    background: var(--discord-lighter-color);
    border-radius: 6px;
    display: grid;
    padding: 1rem 1rem 2rem;
  }

  .author {
    margin-left: 15px;
    display: flex;
    align-items: center;
    gap: .5em;

    h1 {
      font-size: .5rem;
      font-weight: 500;
    }

    svg {
      width: 32px;
    }

    img {
      height: 1.2em;
      width: 1.2em;
    }

    p {
      font-size: .75em;
      margin: 0;
    }

    .name {
      font-size: .75em;
      font-weight: bold;
    }

    .command-used {
      color: var(--text-color-secondary);

      span {
        padding: 0;
        font-weight: bold;
        color: var(--button-color);
      }
    }
  }

  .sender {
    display: flex;
    align-items: center;
    gap: .5em;

    h1 {
      font-size: 0.8em;
      font-weight: 500
    }

    p {
      font-size: 0.75em;
      color: var(--text-color-secondary);
    }

    img {
      margin-right: 1em;
      height: 32px;
      width: 32px;
    }
  }

  .embed {
    font-size: 0.8em;
    margin-left: calc(2em + 32px);
    background-color: var(--header-background-color);
    padding: 1em 1.5em;
    border-radius: .4em;
    border-left: .4em solid var(--discord-darker-color);
    width: max-content;
  }

  span {
    padding: .2rem .4rem;
    border-radius: .25rem;
    color: var(--text-color-secondary);

    &.block {
      background: var(--discord-darker-color);
    }

    &.ping {
      background-color: var(--discord-ping-color);
    }

    &.badge {
      background-color: var(--discord-badge-color);
      color: var(--text-color);
      text-transform: uppercase;
      font-size: .75em;
      margin-left: .5em;
    }
  }

</style>
<script>
  export default {
    name: 'Embed'
  }
</script>