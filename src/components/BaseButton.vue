<template>
  <button class="button" :class="typeButton">Free Consultation</button>
</template>

<script>
export default {
  props: {
    typeButton: {
      type: String,
      validator(value) {
        return ['primary', 'secondary'].includes(value);
      },
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../style.scss';

.button {
  width: 228px;
  height: 56px;
  border: none;
  font-size: 16px;
  border-radius: 28px;
  color: $light-cream;
  transition: background-color 0.3s;
}

.primary {
  background-color: $black;
  &:hover {
    background-color: $galactic-blue;
  }
}

.secondary {
  background-color: $light-red;
  &:hover {
    background-color: $summer-yellow;
  }
}
</style>
