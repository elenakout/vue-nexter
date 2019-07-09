<template>
  <div class="challenge">
    <div class="header ">
      Header
    </div>
    <div class="small-box-1">Small box 1</div>
    <div class="small-box-2">Small box 2</div>
    <div class="small-box-3">Small box 3</div>
    <div class="sidebar">Sidebar</div>
    <div class="main">Main content</div>
    <div class="footer">Footer</div>
  </div>
</template>

<style lang="scss" scoped>
.challenge {
  width: 1000px;
  margin: 30px auto;

  display: grid;
  grid-template-rows: 1fr 2fr 4fr 1fr;
  grid-template-columns: repeat(3, 1fr) 20%;
  grid-gap: 30px;

  & > * {
    background-color: orangered;
    padding: 20px;
    font-size: 30px;
    font-family: sans-serif;
    color: white;
  }
}

.header {
  grid-row: 1 / 2;
  grid-column: 1 / -1;
}

.sidebar {
  grid-column: 4 /5;
  grid-row: 2 / 4;
}

.main {
  grid-row: 3 / 4;
  grid-column: 1 / span 3;
}

.footer {
  grid-row: 4 / 5;
  grid-column: 1 / -1;
}
</style>
