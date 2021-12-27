<script setup>
  import BlueButton from '../components/buttons/BlueButton.vue'
</script>
<template>
  <h2>Meet our core team</h2>
  <p>
    The Pincer core team contains the founders and contributors that has been giving a lot of their time to implement
    essentials features of the library. They have an extended knowledge on the most critical features and can help you
    along the way.
  </p>
  <div class="team">
    <figure class="member">
      <img src="img/sigma.png" alt="sigma"/>
      <figcaption>
        <a href="https://github.com/Sigmanificient">Sigmanificient,</a>
        <p>Founder</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/arthurdw.png" alt="arthurdw"/>
      <figcaption>
        <a href="https://github.com/Arthurdw">Arthurdw,</a>
        <p>Co-Founder</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/lunarmagpie.png" alt="lunarmagpie"/>
      <figcaption>
        <a href="https://github.com/Lunarmagpie">Lunarmagpie,</a>
        <p>Main Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/endercheif.png" alt="endercheif"/>
      <figcaption>
        <a href="https://github.com/Endercheif">Endercheif,</a>
        <p>Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/trag1c.png" alt="trag1c"/>
      <figcaption>
        <a href="https://github.com/trag1c">trag1c,</a>
        <p>Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/other.png" alt="someone else"/>
      <figcaption>
        <a href="https://github.com">Maybe You?,</a>
        <p>Future Maintainer</p>
      </figcaption>
    </figure>
  </div>
  <BlueButton text="Apply to join" link="mailto:contact@Pincer.dev"/>
</template>
<style lang="scss" scoped>
h2 {
  margin-top: 40px;
}

.team {
  font-size: 0.6rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin-bottom: 20px;

  a:focus, a:hover {
    text-decoration: underline;
    outline: none;
  }
}

.member {
  display: flex;
  justify-content: flex-start;

  gap: 10px;
  margin: 0;

  p {
    margin: 0;
    text-align: justify;
  }

  img {
    width: 24px;
    height: 24px;
  }
}
</style>
<script>
  export default {
    name: 'Team'
  }
</script>