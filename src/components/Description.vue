<template>
  <main class="description">
    <h1 class="description__header">Design solutions made easy</h1>
    <p class="description__body">
      With over ten years of experience in various design disciplines, I’m your
      one-stop shop for your design needs.
    </p>
  </main>
</template>

<style lang="scss" scoped>
@import '../style.scss';
.description {
  margin-top: 66px;
  text-align: center;

  &__header {
    @include heading-large;
  }
  &__body {
    @include body-medium;
    width: 730px;
    margin: 23px auto 0;
  }
}
</style>
