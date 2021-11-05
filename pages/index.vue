<template>
  <!-- Landing Page -->
  <section>
    <ul class="landing-links">
      <li>
        <a
          href="https://www.imdb.com/name/nm11906396/"
          target="_blank"
        >IMDb</a>
      </li>
      <li>
        <a
          href="https://resumes.actorsaccess.com/francescabmccormick"
          target="_blank"
        >ACTORS ACCESS</a>
      </li>
      <li>
        <a
          href="https://app.castingnetworks.com/talent/public-profile/b9b305d6-35e3-11ec-9c45-2b5241d49a43"
          target="_blank"
        >LA CASTING</a>
      </li>
      <li>
        <a
          href="https://www.backstage.com/u/francesca-mccormick/"
          target="_blank"
        >BACKSTAGE</a>
      </li>
    </ul>
    <img
      class="landing-image"
      src="@/assets/images/landingfran.jpg"
      alt="Fran at Vogue Event"
    >
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
/* Landing Page */
.landing-image {
  margin-top: -4rem;
  height: 100%;
  width: 100%;
  border: 4rem solid #ad2a67;
  border-radius: 4px;
}

.landing-links {
  margin-top: -4rem;
  list-style: none;
  display: flex;
  justify-content: space-around;
  padding: 1rem 0;
  font-family: "crushed", Arial, Helvetica, sans-serif;
  li {
    padding: 2rem;
    &:hover {
      background-color: white;
    }
  }
  a {
    font-size: 2.5rem;
    color: #ad2a67;
    text-decoration: none;
  }
}

@media screen and (max-width: 900px) {
  .landing-image {
    border: 0.5rem solid #ad2a67;
  }

  .landing-links {
    align-items: center;
    a {
      font-size: 0.8rem;
    }
  }

}
</style>
