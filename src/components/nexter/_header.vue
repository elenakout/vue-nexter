<template>
  <div class="header-comp">
    <img
      src="../../assets/img/logo.png"
      alt="Nexter logo"
      class="header__logo"
    />
    <h3 class="heading-3">Your own home:</h3>
    <h1 class="heading-1">The ultimate personal freedom</h1>
    <button class="btn header__btn">View our properties</button>
    <div class="header__seenon-text">Seen on</div>
    <div class="header__seenon-logos">
      <img
        v-for="(logo, idx) in logos"
        :key="idx"
        :src="logo"
        alt="Seen on logo"
      />
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
  padding: 8rem;
  padding-top: 4rem;

  display: grid;
  grid-template-rows: 1fr min-content minmax(6rem, min-content) 1fr;
  grid-template-columns: minmax(min-content, max-content);
  grid-row-gap: 1.5rem;
  justify-content: center;

  .header {
    &__logo {
      height: 3rem;
      justify-self: center;
    }

    &__btn {
      align-self: start;
      justify-self: start;
    }

    &__seenon-text {
      display: grid;
      grid-template-columns: 1fr max-content 1fr;
      align-items: center;
      grid-column-gap: 1.5rem;

      font-size: 1.6rem;
      color: var(--color-grey-light-2);

      &::before,
      &::after {
        content: "";
        height: 1px;
        display: block;
        background-color: currentColor;
      }
    }

    &__seenon-logos {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-column-gap: 3rem;
      justify-items: center;
      align-items: center;

      img {
        max-height: 2.5rem;
        max-width: 100%;
        filter: brightness(70%);
      }
    }
  }
}
</style>
