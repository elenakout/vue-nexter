<template>
  <div class="header-comp">
    <img
      src="../../assets/img/logo.png"
      alt="Nexter logo"
      class="header__logo"
    />
    <h3 class="heading-3">Your own home:</h3>
    <h1 class="heading-1">The ultimate personal freedom</h1>
    <button class="btn">View our properties</button>
    <div class="header__seenon-text">Seen on</div>
    <div class="header__seenon-logos" v-for="(logo, idx) in logos" :key="idx">
      <img :src="logo" alt="Seen on logo" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logos: [
        require("@/assets/img/logo-bbc.png"),
        require("@/assets/img/logo-forbes.png"),
        require("@/assets/img/logo-techcrunch.png"),
        require("@/assets/img/logo-bi.png")
      ]
    };
  }
};
</script>

<style lang="scss">
.header-comp {
  height: 100%;
  background-color: var(--color-grey-dark-1);
  background-image: linear-gradient(rgba(#101d2c, 0.93), rgba(#101d2c, 0.93)),
    url(../../assets/img/hero.jpeg);
  background-size: cover;
  background-position: center;

  .header {
    &__logo {
      height: 3rem;
    }

    &__seenon-text {
    }

    &__seenon-logos {
      img {
        height: 2.5rem;
      }
    }
  }
}
</style>
