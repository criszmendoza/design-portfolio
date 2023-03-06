<template>
  <header class="container nav-bar">
    <img class="nav-bar__icon" src="../assets/logo.svg" />
    <base-button typeButton="primary" />
  </header>
</template>

<style lang="scss" scoped>
.nav-bar {
  align-items: center;
  display: flex;
  height: 64px;
  justify-content: space-between;

  &__icon {
    height: 64px;
    width: 64px;
  }
}
</style>
