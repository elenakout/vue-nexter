<template>
  <div class="features-comp">
    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-global"></use>
      </svg>
      <h4 class="heading-4">World's best luxury homes</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio officiis
        voluptates repudiandae quos.
      </p>
    </div>

    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-trophy"></use>
      </svg>
      <h4 class="heading-4">Only the best properties</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse rem
        accusantium dolores ratione minima?
      </p>
    </div>

    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-map-pin"></use>
      </svg>
      <h4 class="heading-4">All homes in top locations</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </p>
    </div>

    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-key"></use>
      </svg>
      <h4 class="heading-4">New home in one week</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium id
        doloribus fuga officia asperiores?
      </p>
    </div>

    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-presentation"></use>
      </svg>
      <h4 class="heading-4">Top 1% realtors</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam, aliquid
        aliquam.
      </p>
    </div>

    <div class="feature">
      <svg class="feature__icon">
        <use xlink:href="../../assets/img/sprite.svg#icon-lock"></use>
      </svg>
      <h4 class="heading-4">Secure payments on nexter</h4>
      <p class="feature__text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.features-comp {
  margin: 15rem;

  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 6rem;
}
</style>
