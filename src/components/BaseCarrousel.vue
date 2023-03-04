<template>
  <div class="carrousel">
    <div class="carrousel__items" ref="carrousel">
      <article class="card">
        <img src="../assets/image-slide-1.jpg" alt="slide-1" />
      </article>
      <article class="card">
        <img src="../assets/image-slide-2.jpg" alt="slide-2" />
      </article>
      <article class="card">
        <img src="../assets/image-slide-3.jpg" alt="slide-3" />
      </article>
      <article class="card">
        <img src="../assets/image-slide-4.jpg" alt="slide-4" />
      </article>
      <article class="card">
        <img src="../assets/image-slide-5.jpg" alt="slide-5" />
      </article>
    </div>

    <div class="carrousel__controls">
      <base-arrow class="carrousel__arrow" direction="left" @action="left" />
      <base-arrow class="carrousel__arrow" direction="right" @action="right" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      position: null,
    };
  },
  methods: {
    right() {
      this.$refs.carrousel.scrollLeft += window.screen.width / 4;
    },
    left() {
      this.$refs.carrousel.scrollLeft -= window.screen.width / 4;
    },
  },
  mounted() {
    this.$refs.carrousel.scrollLeft = window.screen.width / 2;
  },
};
</script>

<style lang="scss" scoped>
.carrousel {
  &__items {
    margin-top: 56px;
    display: grid;
    grid-auto-flow: column;
    scroll-behavior: auto;
    gap: 1.2rem;
    overflow: hidden;
  }

  &__controls {
    margin-top: 56px;
    text-align: center;
  }
  &__arrow {
    margin: 0 8px;
  }
}

.card {
  width: 540px;
  height: 360px;
  height: 360px;
}
</style>
