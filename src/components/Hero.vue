<template>
  <section class="hero container">
    <img class="hero__img" src="../assets/image-amy.webp" />
    <div class="hero__description">
      <h2>I’m Amy, and I’d love to work on your next project</h2>
      <p>
        I love working with others to create beautiful design solutions. I’ve
        designed everything from brand illustrations to complete mobile apps.
        I’m also handy with a camera!
      </p>
      <base-button typeButton="secondary" />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import '../style.scss';

.hero {
  margin-top: 136px;
  display: flex;
  align-items: center;
  &__img {
    height: 445px;
    width: 445px;
  }
  &__description {
    width: 540px;
    margin-left: auto;
    text-align: start;
    h2 {
      @include heading-medium;
    }
    p {
      margin-top: 34px;
      margin-bottom: 32px;
      @include body-medium;
    }
  }
}
</style>
