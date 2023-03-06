<template>
  <div class="skill" :class="[size, name]">
    <img :alt="title" class="skill__icon" :src="img" />
    <p class="skill__title">{{ title }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    img: {
      type: String,
      required: true,
    },
    size: {
      type: String,
      validator(value) {
        return ['small', 'medium', 'big'].includes(value);
      },
    },
  },
  computed: {
    name() {
      return this.title.replace(' ', '-').replace('/', '-').toLowerCase();
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../style.scss';
.skill {
  color: $light-cream;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 24px;

  &__title {
    font-family: 'Plus Jakarta Sans';
    font-size: 24px;
    font-weight: 700;
    justify-self: end;
    letter-spacing: 0px;
    line-height: 30px;
    text-align: left;
  }

  &__icon {
    align-self: end;
  }
}
.small {
  border-radius: 8px;
  .skill__icon {
    width: 64px;
    height: 64px;
  }
}
.medium {
  border-radius: 8px;
  .skill__icon {
    width: 128px;
    height: 64px;
  }
}
.big {
  border-radius: 8px;
  .skill__icon {
    height: 192px;
    width: 128px;
  }
}

.graphic-design {
  background-color: $galactic-blue;
  grid-area: graphic-design;
}
.ui-ux {
  background-color: $summer-yellow;
  grid-area: ui-ux;
}
.apps {
  background-color: $pink;
  grid-area: apps;
}
.photography {
  background-color: $cyan;
  grid-area: photography;
}
.illustrations {
  background-color: $light-red;
  grid-area: illustrations;
}
.motion-graphics {
  background-color: $purple;
  grid-area: motion-graphics;
}
</style>
