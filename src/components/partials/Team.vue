<template>
  <div class="team-container">
    <h2>Meet our core team</h2>
    <p>
      The Pincer core team contains the founders and contributors that have been
      giving a lot of their time to implement the essential features of the
      library. They have an extended knowledge on the most critical features and
      can help you along the way.
    </p>
    <div class="team">
      <figure class="team-member">
        <img src="@/assets/members/Sigma.png" alt="sigma" />
        <figcaption>
          <a href="https://github.com/Sigmanificient">Sigmanificient</a>
          <p>Founder</p>
        </figcaption>
      </figure>
      <figure class="team-member">
        <img src="@/assets/members/Arthurdw.png" alt="arthurdw" />
        <figcaption>
          <a href="https://github.com/Arthurdw">Arthurdw</a>
          <p>Co-Founder</p>
        </figcaption>
      </figure>
      <figure class="team-member">
        <img src="@/assets/members/Lunarmagpie.png" alt="lunarmagpie" />
        <figcaption>
          <a href="https://github.com/Lunarmagpie">Lunarmagpie</a>
          <p>Main Maintainer</p>
        </figcaption>
      </figure>
      <figure class="team-member">
        <img src="@/assets/members/Endercheif.png" alt="endercheif" />
        <figcaption>
          <a href="https://github.com/Endercheif">Endercheif</a>
          <p>Maintainer</p>
        </figcaption>
      </figure>
      <figure class="team-member">
        <img src="@/assets/members/trag1c.png" alt="trag1c" />
        <figcaption>
          <a href="https://github.com/trag1c">trag1c</a>
          <p>Maintainer</p>
        </figcaption>
      </figure>
      <figure class="team-member">
        <img src="@/assets/members/_other.png" alt="someone else" />
        <figcaption>
          <a href="https://github.com">Maybe You?</a>
          <p>Future Maintainer</p>
        </figcaption>
      </figure>
    </div>
    <BlueButton text="Apply To Join" link="mailto:contact@Pincer.dev" />
  </div>
</template>

<script>
import BlueButton from "@/components/buttons/Btn.vue";

export default {
  name: "Team",
  components: {
    BlueButton,
  },
};
</script>

<style lang="scss">
.team {
  font-size: 0.6rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4em;
  margin-top: 6em;
  margin-bottom: 6em;
  place-items: center;

  &-member {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    width: 120px;
    gap: 10px;
    margin: 0;

    a {
      font-size: 1.2em;
    }

    p {
      margin: 0;
      text-align: justify;
      font-size: 1em;
    }

    img {
      width: clamp(24px, 5vw, 48px);
      height: clamp(24px, 5vw, 48px);
    }
  }

  &-container {
    position: relative;

    &::before {
      content: "";
      inset: 0;
      position: absolute;
      background: url("../../assets/decorations/wave.svg") no-repeat 50% 60%;
      background-size: 75%;
      z-index: -1;
      opacity: 0.2;
    }

    h2 {
      margin-top: 40px;
    }
  }

  a:focus,
  a:hover {
    text-decoration: underline;
    outline: none;
  }
}

@media (min-width: 820px) {
  .team {
    grid-template-columns: 1fr 1fr 1fr;

    &-container {
      margin: 0 4em;
    }

    &-member {
      width: 200px;
    }
  }
}
</style>
