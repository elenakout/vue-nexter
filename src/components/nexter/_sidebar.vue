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
}
</style>
