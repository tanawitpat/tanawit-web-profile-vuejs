<template>
  <section class="section-skills">
    <div class="bg-video">
      <video class="bg-video__content" autoplay muted loop>
        <source src="../../assets/img/Love-Coding.mp4" type="video/mp4" />
        <source src="../../assets/img/Love-Coding.webm" type="video/webm" />
      </video>
    </div>
    <h1 class="heading-primary u-margin-bottom-medium section-skills__heading">Skills</h1>
    <div class="section-skills__cards">
      <SkillCategory
        v-for="category in skillData"
        :key="category.name"
        :categoryName="category.name"
        :skills="category.items"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SkillCategory from './components/SkillCategory.vue';
import skillData from '@/assets/data/skill.json';

export default {
  name: 'section-skill',
  data() {
    return {
      skillData: skillData.data,
    };
  },
  components: {
    SkillCategory,
  },
};
</script>

<style scoped lang="scss">
.section-skills {
  padding: 10rem 15rem;
  position: relative;
  background-color: rgba($color-blue-dark, 0.85);

  @include respond(medium) {
    padding: 10rem 5rem;
  }

  @include respond(small) {
    padding: 10rem 3rem;
  }

  &__heading {
    color: #fff;
  }

  &__cards {
    color: #fff;
    max-width: 120rem;
    margin: 0 auto;

    display: grid;
    grid-template-columns: repeat(2, 1fr);

    @include respond(largest) {
      grid-template-columns: 1fr;
    }
  }
}

.bg-video {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: -1;
  opacity: 0.8;
  overflow: hidden;

  &__content {
    height: 100%;
    width: 100%;
    object-fit: cover;
  }
}
</style>
