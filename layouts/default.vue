<template>
  <div id="app">
    <Navbar />
    <main class="main">
      <Nuxt />
    </main>
  </div>
</template>

<style lang="scss">
html {
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

@font-face {
  font-family: "AmsterdamOne";
  src: url("./assets/fonts/amsterdamOne.ttf");
}

@font-face {
  font-family: "crushed";
  src: url("./assets/fonts/crushed.ttf");
}

body {
  margin: 0;
  background-color: #fad0c6;
  font-family: "Open Sans", Arial, Helvetica, sans-serif;
}

h2 {
  font-family: "crushed", Arial, Helvetica, sans-serif;
  font-size: 6rem;
  color: #2e3138;
}

.header-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Main Section */

.main {
  padding: 8rem 10rem;
}

@media screen and (max-width: 900px) {
  .main {
    padding: 6rem 1rem;
  }

  h2 {
    font-size: 3.75rem;
  }
}
</style>
