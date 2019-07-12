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
      <button class="btn">Contact realtor</button>
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
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-1.jpeg"
        },
        {
          name: "Modern Glass Villa",
          price: "2.750.000",
          location: "Canada",
          rooms: 6,
          area: 450,
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-2.jpeg"
        },
        {
          name: "Cozy Country House",
          price: "850.000",
          location: "UK",
          rooms: 4,
          area: 250,
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-3.jpeg"
        },
        {
          name: "Large Rustical Villa",
          price: "1.950.000",
          location: "Portugal",
          rooms: 18,
          area: 480,
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-4.jpeg"
        },
        {
          name: "Majestic Palace House",
          price: "9.500.000",
          location: "Germany",
          rooms: 18,
          area: 4320,
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-5.jpeg"
        },
        {
          name: "Modern Family Apartment",
          price: "600.000",
          location: "Italy",
          rooms: 3,
          area: 180,
          img:
            "https://raw.githubusercontent.com/jonasschmedtmann/advanced-css-course/master/Nexter/starter/img/house-6.jpeg"
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

  &__img {
    width: 100%;
  }

  &__like {
  }

  &__name {
  }

  &__location,
  &__rooms,
  &__area,
  &__price {
    svg {
      fill: var(--color-primary);
      height: 2rem;
      width: 2rem;
    }
    p {
    }
  }
}
</style>
