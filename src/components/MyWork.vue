<template>
  <section class="my-work">
    <h3>My work</h3>
    <base-carrousel />
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import '../style.scss';

.my-work {
  margin-top: 88px;

  h3 {
    @include heading-small;
    text-align: center;
  }
}
</style>
