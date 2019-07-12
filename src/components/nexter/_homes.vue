<template>
  <div class="homes-comp">
    <div v-for="(home, idx) in homes" :key="idx" class="home">
      <img :src="home.img" alt="house pic " class="home__img" />
      <svg class="home__like">
        <use xlink:href="../../assets/img/sprite.svg#icon-heart-full"></use>
      </svg>
      <h5 class="home__name">{{ home.name }}</h5>
      <div class="home__location">
        <svg>
          <use xlink:href="../../assets/img/sprite.svg#icon-map-pin"></use>
        </svg>
        <p>{{ home.location }}</p>
      </div>
      <div class="home__rooms">
        <svg>
          <use xlink:href="../../assets/img/sprite.svg#icon-profile-male"></use>
        </svg>
        <p>{{ home.rooms }}</p>
      </div>
      <div class="home__area">
        <svg>
          <use xlink:href="../../assets/img/sprite.svg#icon-expand"></use>
        </svg>
        <p>{{ home.area }} m<sup>2</sup></p>
      </div>
      <div class="home__price">
        <svg>
          <use xlink:href="../../assets/img/sprite.svg#icon-key"></use>
        </svg>
        <p>${{ home.price }}</p>
      </div>
      <button class="btn home__button">Contact realtor</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      homes: [
        {
          name: "Beautiful Family House",
          price: "1.200.000",
          location: "USA",
          rooms: 5,
          area: 325,
          img: require("@/assets/img/house-1.jpeg")
        },
        {
          name: "Modern Glass Villa",
          price: "2.750.000",
          location: "Canada",
          rooms: 6,
          area: 450,
          img: require("@/assets/img/house-2.jpeg")
        },
        {
          name: "Cozy Country House",
          price: "850.000",
          location: "UK",
          rooms: 4,
          area: 250,
          img: require("@/assets/img/house-3.jpeg")
        },
        {
          name: "Large Rustical Villa",
          price: "1.950.000",
          location: "Portugal",
          rooms: 6,
          area: 480,
          img: require("@/assets/img/house-4.jpeg")
        },
        {
          name: "Majestic Palace House",
          price: "9.500.000",
          location: "Germany",
          rooms: 18,
          area: 4320,
          img: require("@/assets/img/house-5.jpeg")
        },
        {
          name: "Modern Family Apartment",
          price: "600.000",
          location: "Italy",
          rooms: 3,
          area: 180,
          img: require("@/assets/img/house-6.jpeg")
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.homes-comp {
  margin: 15rem 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
  grid-gap: 7rem;
}

.home {
  background-color: var(--color-grey-light-1);

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-row-gap: 3.5rem;

  &__img {
    width: 100%;
    grid-row: 1 / 2;
    grid-column: 1 / -1;
    z-index: 1;
  }

  &__like {
    fill: var(--color-primary);
    height: 2.5rem;
    width: 2.5rem;
    grid-row: 1 / 2;
    grid-column: 2 / 3;
    justify-self: end;
    margin: 1rem;
    z-index: 2;
  }

  &__name {
    background-color: var(--color-secondary);
    font-family: var(--font-display);
    font-size: 1.6rem;
    text-align: center;
    padding: 1.25rem;
    color: #fff;
    font-weight: 400;
    width: 80%;
    transform: translateY(50%);

    justify-self: center;
    align-self: end;

    grid-row: 1 / 2;
    grid-column: 1 / -1;
    z-index: 3;
  }

  &__location,
  &__rooms {
    margin-top: 2.5rem;
  }

  &__location,
  &__rooms,
  &__area,
  &__price {
    font-size: 1.5rem;
    margin-left: 2rem;
    display: flex;
    align-items: center;

    svg {
      fill: var(--color-primary);
      height: 2rem;
      width: 2rem;
      margin-right: 1rem;
    }
  }

  &__button {
    grid-column: 1 / -1;
  }
}
</style>
