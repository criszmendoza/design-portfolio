<template>
  <header class="container nav-bar">
    <img class="nav-bar__icon" src="../assets/logo.svg" />
    <base-button typeButton="primary" />
  </header>
</template>

<style lang="scss" scoped>
.nav-bar {
  height: 64px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__icon {
    width: 64px;
    height: 64px;
  }
}
</style>
