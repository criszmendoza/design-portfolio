<template>
  <section class="container">
    <div class="skills-list">
      <skill-item
        v-for="skill in skills"
        :title="skill.title"
        :key="skill.title"
        :size="skill.size"
        :img="skill.img"
      />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        {
          title: 'Graphic Design',
          size: 'big',
          img: '/pattern-graphic-design.svg',
        },
        {
          title: 'UI/UX',
          size: 'small',
          img: '/pattern-ui-ux.svg',
        },
        {
          title: 'Apps',
          size: 'small',
          img: '/pattern-apps.svg',
        },
        {
          title: 'Photography',
          size: 'medium',
          img: '/pattern-photography.svg',
        },
        {
          title: 'Illustrations',
          size: 'medium',
          img: '/pattern-illustrations.svg',
        },
        {
          title: 'Motion Graphics',
          size: 'medium',
          img: '/pattern-motion-graphics.svg',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.skills-list {
  margin-top: 80px;
  width: 100%;
  height: 364px;
  display: grid;
  gap: 24px;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-template-areas:
    'graphic-design graphic-design ui-ux apps photography photography'
    'graphic-design graphic-design illustrations illustrations motion-graphics motion-graphics';

  @media (max-width: 1024px) {
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(3, 1fr);
    height: 570px;
    grid-template-areas:
      'graphic-design graphic-design ui-ux apps'
      'graphic-design graphic-design illustrations illustrations'
      'photography photography  motion-graphics motion-graphics';
  }

  @media (max-width: 628px) {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(6, 1fr);
    height: 1164px;
    grid-template-areas:
      'graphic-design graphic-design'
      'graphic-design graphic-design'
      'ui-ux apps'
      'illustrations illustrations'
      'photography photography'
      'motion-graphics motion-graphics';
  }
}
</style>
