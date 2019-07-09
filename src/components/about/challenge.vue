<template>
  <div class="challenge">
    <div class="header grid-item">
      Header
    </div>
    <div class="small-box-1 grid-item">Small box 1</div>
    <div class="small-box-2 grid-item">Small box 2</div>
    <div class="small-box-3 grid-item">Small box 3</div>
    <div class="sidebar grid-item">Sidebar</div>
    <div class="main grid-item">Main content</div>
    <div class="footer grid-item">Footer</div>
  </div>
</template>

<style lang="scss" scoped>
.challenge {
  padding: 50px;
  font-size: 30px;
  font-family: sans-serif;
  color: white;

  display: grid;
  grid-template-rows: 1fr 3fr 4fr 1fr;
  grid-template-columns: repeat(3, 1fr) 20%;
  grid-gap: 30px;
}

.grid-item {
  background-color: orangered;
  padding: 20px;
}

.header {
  grid-row: 1 / 2;
  grid-column: 1 / -1;
}

.sidebar {
  grid-row: 2 / 4;
}

.main {
  grid-row: 3 / 4;
  grid-column: 1 / 4;
}

.footer {
  grid-row: 4 / 5;
  grid-column: 1 / -1;
}
</style>
