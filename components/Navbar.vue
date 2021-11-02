<template>
  <!-- Nav Bar -->
  <nav>
    <ul>
      <li>
        <NuxtLink to="/">
          <div class="logo">
            <span class="highlight">Francesca</span>
            <span class="subtext">Barker McCormick</span>
          </div>
        </NuxtLink>
      </li>
      <li
        v-for="tab in tabs"
        :key="tab"
        class="nav-links"
      >
        <NuxtLink :to="`/${tab.toLowerCase()}`">
          {{ tab }}
        </NuxtLink>
      </li>
      <li class="mobile-nav">
        <a href="javascript:void(0);" class="mobile-menu" @click="showNav()">
          <font-awesome-icon :icon="['fas', 'bars']" />
        </a>
      </li>
    </ul>
    <ul v-show="toggleMobileNav === true" class="mobile-links">
      <li
        v-for="tab in tabs"
        :key="tab"
        class="mobile-link"
      >
        <NuxtLink :to="`/${tab.toLowerCase()}`">
          {{ tab }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      toggleMobileNav: false,
      tabs: ['About', 'Photos', 'Video', 'Resume', 'Reviews', 'Contact']
    }
  },
  watch: {
    $route () {
      this.toggleMobileNav = false
    }
  },
  methods: {
    showNav () {
      this.toggleMobileNav = !this.toggleMobileNav
    }
  }
}
</script>

<style lang="scss" scoped>
/* Navigation */

nav {
  font-family: "AmsterdamOne", sans-serif;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  margin: 0;
  background-color: #ad2a67;
  border-bottom: 0.5rem solid #f56200;
}

nav ul {
  display: flex;
  justify-content: space-evenly;
  list-style: none;
}

.mobile-nav {
  display: none;

  a {
    text-decoration: none;
    color: #fad0c6;
  }
}

.highlight {
  color: #2e3138;
}

/* .subtext {
    font-family: 'crushed';
    position: absolute;
} */

nav li {
  padding: 1.25rem;
  margin: 0 0.3125rem;
  font-size: 1.25rem;
  cursor: pointer;
}

nav li a {
  color: #fad0c6;
  text-decoration: none;
}

nav li a:hover {
  color: #f56200;
}

@media screen and (max-width: 900px) {
nav ul {
    justify-content: space-around;
    align-items: center;
    padding: 0;
  }

  nav li {
    padding: 0;
    margin: 0;
  }

  .mobile-nav {
    display: block;
    padding: 0.5rem;
    font-size: 1.5rem;
  }

  .mobile-links {
    background-color: #ad2a67;
    padding: 0;
    position: absolute;
    top: 7.6rem;
    text-align: center;
    display: block;
    width: 100%;
  }

  .mobile-link {
    font-family: "AmsterdamOne", sans-serif;
    padding: 0.7rem;
    font-size: 1rem;
    color: #fad0c6;
    list-style: none;
  }

  .nav-links {
    display: none;
  }

  .logo {
    font-size: 1rem;
  }
}
</style>
