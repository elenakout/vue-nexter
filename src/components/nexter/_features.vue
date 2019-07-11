<template>
  <div class="features-comp">
    <div class="feature" v-for="(item, idx) in features" :key="idx">
      <svg class="feature__icon">
        <use
          v-if="item.icon === 'global'"
          href="../../assets/img/sprite.svg#icon-global"
        ></use>
        <use
          v-if="item.icon === 'trophy'"
          href="../../assets/img/sprite.svg#icon-trophy"
        ></use>
        <use
          v-if="item.icon === 'map-pin'"
          href="../../assets/img/sprite.svg#icon-map-pin"
        ></use>
        <use
          v-if="item.icon === 'key'"
          href="../../assets/img/sprite.svg#icon-key"
        ></use>
        <use
          v-if="item.icon === 'presentation'"
          href="../../assets/img/sprite.svg#icon-presentation"
        ></use>
        <use
          v-if="item.icon === 'lock'"
          href="../../assets/img/sprite.svg#icon-lock"
        ></use>
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
          icon: "global"
        },
        {
          heading: "Only the best properties",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse rem accusantium dolores ratione minima?",
          icon: "trophy"
        },
        {
          heading: "All homes in top locations",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          icon: "map-pin"
        },
        {
          heading: "New home in one week",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium id doloribus fuga officia asperiores?",
          icon: "key"
        },
        {
          heading: "Top 1% realtors",
          text:
            "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam, aliquid aliquam.",
          icon: "presentation"
        },
        {
          heading: "Secure payments on nexter",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          icon: "lock"
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

.feature {
  &__icon {
    fill: var(--color-primary);
    width: 4.5rem;
    height: 4.5rem;
  }

  &__text {
    font-size: 1.7rem;
  }
}
</style>
