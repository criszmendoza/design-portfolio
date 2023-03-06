<template>
  <main class="container">
    <div class="description">
      <h1 class="description__header">Design solutions made easy</h1>
      <p class="description__body">
        With over ten years of experience in various design disciplines, I’m
        your one-stop shop for your design needs.
      </p>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@import '../style.scss';
.description {
  margin: 66px auto 0;
  max-width: 751px;
  min-width: 288px;
  text-align: center;

  &__header {
    @include heading-large;
  }
  &__body {
    @include body-medium;
    margin: 23px auto 0;
    width: 92%;

    @media (max-width: 768px) {
      width: 82%;
    }
  }
}
</style>
