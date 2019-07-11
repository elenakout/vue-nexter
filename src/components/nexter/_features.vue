<template>
  <div class="features-comp">
    <div class="feature" v-for="(item, idx) in features" :key="idx">
      <svg class="feature__icon">
        <use href="../../assets/img/sprite.svg#icon-global"></use>
      </svg>
      <h4 class="heading-4">{{ item.heading }}</h4>
      <p class="feature__text">
        {{ item.text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          heading: "World's best luxury homes",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio officiis voluptates repudiandae quos.",
          icon: "../../assets/img/sprite.svg#icon-global"
        },
        {
          heading: "Only the best properties",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse rem accusantium dolores ratione minima?",
          icon: "../../assets/img/sprite.svg#icon-trophy"
        },
        {
          heading: "All homes in top locations",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          icon: "../../assets/img/sprite.svg#icon-map-pin"
        },
        {
          heading: "New home in one week",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium id doloribus fuga officia asperiores?",
          icon: "../../assets/img/sprite.svg#icon-key"
        },
        {
          heading: "Top 1% realtors",
          text:
            "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam, aliquid aliquam.",
          icon: "../../assets/img/sprite.svg#icon-presentation"
        },
        {
          heading: "Secure payments on nexter",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          icon: "../../assets/img/sprite.svg#icon-lock"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.features-comp {
  margin: 15rem;

  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 6rem;
}
</style>
