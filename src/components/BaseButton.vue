<template>
  <button class="button" :class="typeButton" @click="$emit('action')">
    Free Consultation
  </button>
</template>

<script>
export default {
  props: {
    typeButton: {
      type: String,
      required: true,
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
  border-radius: 28px;
  border: none;
  color: $light-cream;
  font-size: 16px;
  height: 56px;
  min-height: 56px;
  min-width: 228px;
  transition: background-color 0.3s;
  width: 228px;
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
