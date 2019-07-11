<template>
  <div class="story__pictures-comp">
    <img
      src="../../assets/img/story-1.jpeg"
      alt="Couple with a new house"
      class="story__img--1"
    />
    <img
      src="../../assets/img/story-2.jpeg"
      alt="New House"
      class="story__img--2"
    />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.story {
  &__pictures-comp {
    height: 100%;
    // background-color: var(--color-primary);
    background-image: linear-gradient(rgba(#c69963, 0.5), rgba(#c69963, 0.5)),
      url(../../assets/img/back.jpg);

    display: grid;
    grid-template-rows: repeat(6, 1fr);
    grid-template-columns: repeat(6, 1fr);
    align-items: center;
  }

  &__img--1 {
    width: 100%;
    grid-row: 2 /6;
    grid-column: 2 / 6;
    box-shadow: 0 2rem 5rem rgba(#000, 0.1);
  }
  &__img--2 {
    width: 115%;
    grid-row: 4 / 6;
    grid-column: 4 / 7;
    z-index: 100;
    box-shadow: 0 2rem 5rem rgba(#000, 0.2);
  }
}
</style>
