<template>
  <section class="container">
    <div class="skills-list">
      <skill-item
        v-for="skill in skills"
        :title="skill.title"
        :key="skill.title"
        :size="skill.size"
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
        },
        {
          title: 'UI/UX',
          size: 'small',
        },
        {
          title: 'Apps',
          size: 'small',
        },
        {
          title: 'Photography',
          size: 'medium',
        },
        {
          title: 'Illustrations',
          size: 'medium',
        },
        {
          title: 'Motion Graphics',
          size: 'medium',
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
}
</style>
