<template>
  <div class="related">
    <h2>Related projects</h2>

    <div class="related-container">
      <div class="related-container-left">
        <h3>The Pincer CLI</h3>
        <p>
          In the intent to simplify Pincer user life, we are building a console
          line interface tools that will bring automation to the Pincer package.
          Commands to import templates, create cogs and commands are going to
          make the developer experience easier and straight forward, faster and
          open to beginners.
        </p>
        <BlueButton
          text="GitHub Repository"
          link="https://github.com/Pincer-org/cli"
        />
      </div>
      <div class="related-container-right">
        <h3>The Pincer Bot</h3>
        <p>
          Our Discord server needs a powerful yet fun bot to interact with and
          demonstrate the key features of our library. It will also be a good
          example for an advanced bot, running in production, that new users can
          explore to understand how they can use the library and take advantage
          of it.
        </p>
        <BlueButton
          text="GitHub Repository"
          link="https://github.com/Pincer-org/bot"
        />
      </div>
    </div>
  </div>
</template>

<script>
import BlueButton from "@/components/buttons/Btn.vue";

export default {
  name: "Related",
  components: {
    BlueButton,
  },
};
</script>

<style lang="scss">
.related {
  margin-bottom: 4em;

  &-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    gap: 40px;

    &-left {
      position: relative;

      &::before {
        content: "";
        position: absolute;
        inset: 0;

        background: url("../../assets/decorations/cli.svg") no-repeat center;
        background-size: 75% 75%;
        z-index: -1;
        opacity: 0.2;
      }
    }

    &-right {
      margin: 40px 0;
      position: relative;

      &::before {
        content: "";
        position: absolute;
        inset: 0;

        background: url("../../assets/decorations/robot.svg") no-repeat center;
        background-size: 75% 75%;
        z-index: -1;
        opacity: 0.2;
      }
    }
  }

  h2 {
    margin-bottom: 0;
  }

  h3 {
    margin-top: 0;
    margin-bottom: 0;
  }

  p {
    text-align: justify;
  }
}

@media (min-width: 540px) {
  .related-container {
    flex-direction: row;
  }
}
</style>
