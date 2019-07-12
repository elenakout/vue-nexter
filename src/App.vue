<template>
  <div id="app">
    <div id="nav" class="mainnav">
      <router-link to="/" class="mainnav__item">Home</router-link>
      <router-link to="/about" class="mainnav__item">About</router-link>
      <router-link to="/nexter" class="mainnav__item">Nexter</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
:root {
  // COLOR VARIABLES
  --color-primary: #c69963;
  --color-primary-dark: #b28451;

  --color-secondary: #101d2c;

  --color-grey-light-1: #f9f7f6;
  --color-grey-light-2: #aaa;

  --color-grey-dark-1: #54483a;
  --color-grey-dark-2: #6d5d4b;

  // FONT VARIABLES
  --font-primary: "Nunito", sans-serif;
  --font-display: "Josefin Sans", sans-serif;
}

* {
  margin: 0;
  padding: 0;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

html {
  box-sizing: border-box;
  font-size: 62.5%; // 1rem = 10px (10px/16px=62.5%)
}

body {
  font-family: "Open Sans", sans-serif;
  font-weight: 400;
  line-height: 1.6;
}

.mainnav {
  color: white;
  background-color: rgba(117, 117, 117, 0.808);
  height: 5vh;
  font-size: 1.6rem;

  display: flex;
  justify-content: space-around;
  align-items: center;

  &__item {
    width: 20%;
    text-align: center;
    text-decoration: none;
    color: currentColor;
    font-weight: 600;
    padding: 0 1.5rem;
    // border: 1px solid black;
  }
}
</style>
