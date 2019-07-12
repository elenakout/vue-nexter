<template>
  <div class="gallery-comp">
    <figure class="gallery__item gallery__item--1">
      <img :src="image1" alt="" class="gallery__img" />
    </figure>
  </div>
</template>

<script>
export default {
  data() {
    return {
      image1: require("@/assets/img/gal-1.jpeg")
    };
  }
};
</script>

<style lang="scss">
.gallery-comp {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-template-rows: repeat(7, 5vw);
  grid-gap: 1.5rem;
  padding: 1.5rem;
}

.gallery {
  &__item {
    &--1 {
      grid-row: 1 / span 2;
      grid-column: 1 / span 2;
    }
  }

  &__img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    display: block;
  }
}
</style>
