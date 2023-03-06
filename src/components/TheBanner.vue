<template>
  <section class="container banner">
    <div class="content">
      <h3>Book a call with me</h3>
      <p>
        I’d love to have a chat to see how I can help you. The best first step
        is for us to discuss your project during a free consultation. Then we
        can move forward from there.
      </p>
    </div>
    <base-button typeButton="secondary" />
  </section>
</template>

<style lang="scss" scoped>
@import '../style.scss';

.banner {
  align-items: center;
  background-color: $black;
  display: flex;
  justify-content: space-between;
  margin-bottom: 56px;
  margin-top: 88px;
  min-height: 320px;
  padding: 80px 65px;

  @media (max-width: 900px) {
    flex-direction: column;
    justify-content: space-evenly;
    margin-bottom: 40px;
    margin-top: 100px;
    padding: 49px 24px;
    text-align: center;
  }

  h3 {
    @include heading-medium;
    color: $light-cream;
  }

  p {
    @include body-medium;
    margin-top: 24px;
    max-width: 540px;

    @media (max-width: 900px) {
      margin: 24px 0;
    }
  }
}
</style>
