<template>
  <div class="create-grid">
    <div class="container">
      <div class="item item--1">1: Orange</div>
      <div class="item item--2">2: Green</div>
      <div class="item item--3">3: Violet</div>
      <div class="item item--4">4: Pink</div>
      <div class="item item--5">5: Blue</div>
      <div class="item item--6">6: Brown</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.create-grid {
  font-size: 1.6rem;
}

.container {
  background-color: #eee;
  width: 1000px;
  margin: 30px auto;

  display: grid;
  // grid-template-rows: 150px 150px;
  grid-template-rows: repeat(2, 150px);
  grid-template-columns: repeat(3, 1fr);

  grid-gap: 30px;
}

.item {
  padding: 20px;
  font-size: 30px;
  font-family: sans-serif;
  color: white;

  &--1 {
    background-color: orangered;
  }

  &--2 {
    background-color: yellowgreen;
  }

  &--3 {
    background-color: blueviolet;
  }

  &--4 {
    background-color: palevioletred;
  }
  &--5 {
    background-color: royalblue;
  }
  &--6 {
    background-color: goldenrod;
    grid-area: 1 / 2 / 2 / 3;
  }
}
</style>
