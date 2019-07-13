<template>
  <div class="sidebar-comp">
    <button class="nav-btn"></button>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.sidebar-comp {
  display: flex;
  justify-content: center;

  @media only screen and (max-width: 62.5em) {
    justify-content: flex-end;
    align-items: center;
  }
}

.nav-btn {
  border: none;
  border-radius: 0;

  background-color: #fff;
  height: 2px;
  width: 4.5rem;
  margin-top: 4rem;

  &::before,
  &::after {
    background-color: #fff;
    height: 2px;
    width: 4.5rem;
    content: "";
    display: block;
  }

  &::before {
    transform: translateY(-1.5rem);
  }
  &::after {
    transform: translateY(1.3rem);
  }

  @media only screen and (max-width: 62.5em) {
    margin-top: 2.8rem;
    margin-right: 3rem;
    &::before {
      transform: translateY(-1.2rem);
    }
    &::after {
      transform: translateY(1rem);
    }
  }
}
</style>
