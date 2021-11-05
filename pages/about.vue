<template>
  <!-- About Tab -->
  <section>
    <h2>ABOUT ME</h2>
    <div class="about-me">
      <div class="about-me-item">
        <p>
          Francesca Barker McCormick (born April 16, 1993) is a Hispanic
          American actress.
        </p>
        <p>
          Prior to her career in film and television, her inherent eye for
          fashion and shows such as Sweet Home Alabama, Sex and the City,
          Gossip Girl, and The Devil Wears Prada influenced her decision to
          move to New York City to begin work within the luxury fashion
          industry. Francesca produced numerous events with Escada, Vogue,
          GQ, Vanity Fair, Balmain, Fendi, Ralph Lauren, and many more - the
          pinnacle being Vogue’s Met Gala! She also worked as a Vogue Market
          Stylist, acting as a representative of the brand and hosting
          events on their behalf.
        </p>
        <p>
          It was through her hosting of events onscreen and off, that her
          passion for performing ignited once again. After 6 years within
          the corporate fashion world, Francesca gave her acting career
          center stage. Barker McCormick has since landed roles in three
          series pilots (Skylife, SinFull, Justice Soldier of God) and three
          films (Ill Intentions, How to Find Love in a Pandemic, Game of
          Chess).
        </p>
        <p>
          Outside of acting, Francesca continues her work in the event world
          as the Project Director for Gina’s Collective, an advisory for
          tech-enabled nonprofits. She also serves on the event committee
          for the Princess Grace Kelly Foundation, an organization dedicated
          to upholding the legacy of Princess Grace of Monaco, and elevating
          extraordinary emerging artists in theater, dance and film through
          career-advancing grants.
        </p>
        <p>
          She is married to Lee McCormick and together, they have an
          adorable French Bulldog, Penelope.
        </p>
      </div>
      <div class="about-me-item about-me-item-img">
        <div class="about-me-img-frame">
          <img
            class="about-me-img"
            src="@/assets/images/aboutfran.jpg"
            alt="About Francesca"
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    /* About Me Page */

.about-me {
  display: flex;
  justify-content: space-evenly;
  align-items: flex-start;
  color: #2e3138;
  letter-spacing: 0.07em;
}

.about-me-img-frame {
  padding: 0.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.about-me-img {
  border: 1rem solid #2e3138;
  border-radius: 4px;
  width: 20rem;
  /* height: 85%; */
}

.about-me-item {
  padding: 1rem;
  flex: 1 1 0;
}

@media screen and (max-width: 900px) {
.about-me {
    display: flex;
    flex-wrap: wrap;
    letter-spacing: 0.07em;
  }

  .about-me-img-frame {
    background-color: #2e3138;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 4px;
  }

  .about-me-img {
    width: 100%;
    height: 100%;
    border: 0.5rem solid #2e3138;
  }

  .about-me-item {
    padding: 0.5rem;
    flex: 0 1 auto;
    flex-basis: 100%;
  }

  .about-me-item-img {
    margin-top: -2rem;
    order: -1;
  }
}
</style>
