<template>
  <div id="app">
    <div id="nav" class="nav">
      <router-link to="/" class="nav__item">Home</router-link>
      <router-link to="/about" class="nav__item">About</router-link>
      <router-link to="/nexter" class="nav__item">Nexter</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
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

.nav {
  color: white;
  background-color: rgba(117, 117, 117, 0.808);
  height: 5vh;
  font-size: 1.4rem;

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
