<template>
  <div class="gallery-comp">
    <figure
      v-for="(img, idx) in images"
      :key="idx"
      class="gallery__item"
      :class="[img.classname]"
    >
      <img :src="img.image" alt="image" class="gallery__img" />
    </figure>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          image: require("@/assets/img/gal-1.jpeg"),
          classname: "gallery__item--1"
        },
        {
          image: require("@/assets/img/gal-2.jpeg"),
          classname: "gallery__item--2"
        },
        {
          image: require("@/assets/img/gal-3.jpeg"),
          classname: "gallery__item--3"
        },
        {
          image: require("@/assets/img/gal-4.jpeg"),
          classname: "gallery__item--4"
        },
        {
          image: require("@/assets/img/gal-5.jpeg"),
          classname: "gallery__item--5"
        },
        {
          image: require("@/assets/img/gal-6.jpeg"),
          classname: "gallery__item--6"
        },
        {
          image: require("@/assets/img/gal-7.jpeg"),
          classname: "gallery__item--7"
        },
        {
          image: require("@/assets/img/gal-8.jpeg"),
          classname: "gallery__item--8"
        },
        {
          image: require("@/assets/img/gal-9.jpeg"),
          classname: "gallery__item--9"
        },
        {
          image: require("@/assets/img/gal-10.jpeg"),
          classname: "gallery__item--10"
        },
        {
          image: require("@/assets/img/gal-11.jpeg"),
          classname: "gallery__item--11"
        },
        {
          image: require("@/assets/img/gal-12.jpeg"),
          classname: "gallery__item--12"
        },
        {
          image: require("@/assets/img/gal-13.jpeg"),
          classname: "gallery__item--13"
        },
        {
          image: require("@/assets/img/gal-14.jpeg"),
          classname: "gallery__item--14"
        }
      ]
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

    &--2 {
      grid-row: 1 / span 3;
      grid-column: 3 / span 3;
    }

    &--3 {
      grid-row: 1 / span 2;
      grid-column: 6 / span 1;
    }

    &--4 {
      grid-row: 1 / span 2;
      grid-column: 7 / span 2;
    }

    &--5 {
      grid-row: 3 / span 3;
      grid-column: 1 / span 2;
    }

    &--6 {
      grid-row: 4 / span 2;
      grid-column: 3 / span 2;
    }

    &--7 {
      grid-row: 4 / span 1;
      grid-column: 5 / span 1;
    }

    &--8 {
      grid-row: 3 / span 2;
      grid-column: 6 / span 2;
    }

    &--9 {
      grid-row: 3 / span 3;
      grid-column: 8 / span 1;
    }

    &--10 {
      grid-row: 6 / span 2;
      grid-column: 1 / span 1;
    }

    &--11 {
      grid-row: 6 / span 2;
      grid-column: 2 / span 2;
    }

    &--12 {
      grid-row: 6 / span 2;
      grid-column: 4 / span 1;
    }

    &--13 {
      grid-row: 5 / span 3;
      grid-column: 5 / span 3;
    }

    &--14 {
      grid-row: 6 / span 2;
      grid-column: 8 / span 1;
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
