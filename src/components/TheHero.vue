<template>
  <section class="hero container">
    <div class="hero__img">
      <img src="@/assets/image-amy.webp" />
    </div>

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
  align-items: center;
  display: flex;
  justify-content: space-between;
  margin-top: 136px;

  @media (max-width: 768px) {
    margin-top: 102px;
    max-width: none;
    width: 100%;
  }

  @media (max-width: 628px) {
    flex-direction: column;
    margin-top: 100px;
    width: 77.15%;
  }

  &__img {
    padding-right: 69px;
    width: 50%;

    @media (max-width: 628px) {
      padding-right: 0;
      width: 100%;
    }

    img {
      min-width: 300px;
      width: 100%;
    }
  }
  &__description {
    max-width: 540px;
    width: 100%;

    @media (max-width: 628px) {
      margin-top: 40px;
      text-align: center;
    }

    h2 {
      @include heading-medium;
    }
    p {
      @include body-medium;
      margin-bottom: 32px;
      margin-top: 34px;
    }
  }
}
</style>
