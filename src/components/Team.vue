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
        <p>Sigmanificient,</p>
        <p>Founder</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/arthurdw.png" alt="arthurdw"/>
      <figcaption>
        <p>Arthurdw,</p>
        <p>Co-Founder</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/lunarmagpie.png" alt="lunarmagpie"/>
      <figcaption>
        <p>Lunarmagpie,</p>
        <p>Main Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/endercheif.png" alt="endercheif"/>
      <figcaption>
        <p>Endercheif,</p>
        <p>Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/trag1c.png" alt="trag1c"/>
      <figcaption>
        <p>trag1c,</p>
        <p>Maintainer</p>
      </figcaption>
    </figure>
    <figure class="member">
      <img src="img/other.png" alt="someone else"/>
      <figcaption>
        <p>Maybe You?</p>
        <p></p>
      </figcaption>
    </figure>
  </div>
</template>
<style lang="scss" scoped>
.team {
  font-size: 0.6rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin-bottom: 40px;
}

.member {
  display: flex;
  justify-content: flex-start;

  gap: 10px;
  margin: 0;

  p {
    margin: 0;
  }

  img {
    width: 24px;
    height: 24px;
  }
}
</style>
