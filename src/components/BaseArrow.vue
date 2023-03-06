<template>
  <button class="arrow" @click="$emit('action')">
    <img :src="srcImg" alt="Arrow" />
  </button>
</template>

<script>
export default {
  props: {
    direction: {
      type: String,
      required: true,
      validator(value) {
        return ['right', 'left'].includes(value);
      },
    },
  },
  computed: {
    srcImg() {
      return `src/assets/icon-arrow-${this.direction}.svg`;
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../style.scss';

.arrow {
  background-color: $black;
  border-radius: 50%;
  border: none;
  height: 64px;
  transition: background-color 0.3s;
  width: 64px;

  &:hover {
    background-color: $galactic-blue;
  }
}
</style>
