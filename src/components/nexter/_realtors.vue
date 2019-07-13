<template>
  <div class="realtors-comp">
    <h3 class="heading-3 heading">Top 3 Realtors</h3>
    <div class="realtors__list" v-for="(realtor, idx) in realtors" :key="idx">
      <img :src="realtor.img" alt="realtor image" class="realtors__img" />
      <div class="realtors__details">
        <h4 class="heading-4 heading-4--light">{{ realtor.name }}</h4>
        <p class="realtors__sold">{{ realtor.hsold }} houses sold</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      realtors: [
        {
          name: "Erik Feiman",
          hsold: 245,
          img: require("@/assets/img/realtor-1.jpeg")
        },
        {
          name: "Kim Brown",
          hsold: 212,
          img: require("@/assets/img/realtor-2.jpeg")
        },
        {
          name: "Toby Ramsey",
          hsold: 198,
          img: require("@/assets/img/realtor-3.jpeg")
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.realtors-comp {
  height: 100%;
  display: grid;
  padding: 3rem;

  grid-row-gap: 5vh;
  justify-content: center;
  align-content: center;
}

.heading {
  justify-self: center;
}

.realtors {
  &__list {
    display: grid;
    grid-template-columns: min-content max-content;
    grid-column-gap: 2rem;
    align-items: center;
  }

  &__img {
    width: 7rem;
    display: block;
    border-radius: 50%;
  }

  &__sold {
    text-transform: uppercase;
    color: var(--color-grey-light-2);
    margin-top: -3px;
  }
}
</style>
