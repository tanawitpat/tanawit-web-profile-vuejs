<template>
  <section class="section-experience">
    <h1 class="heading-primary u-margin-bottom-big section-experience__heading">Experience</h1>
    <div class="section-experience__card">
      <ExperienceCard
        v-for="item in experienceData"
        :key="item.duration"
        :title="item.title"
        :companyName="item.companyName "
        :duration="item.duration"
        :companyLink="item.companyLink"
        :description="item.description"
        :companyLogoPath="item.companyLogoPath"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ExperienceCard from './components/ExperienceCard.vue';
import experienceData from '@/assets/data/experience.json';

export default {
  name: 'section-experience',
  data() {
    return {
      experienceData: experienceData.data,
    };
  },
  components: {
    ExperienceCard,
  },
};
</script>

<style scoped lang="scss">
.section-experience {
  padding: 10rem;
  position: relative;
  background-image: linear-gradient(
      to right bottom,
      rgba($color-grey-light-1, 0.9),
      rgba(#fff, 0.9)
    ),
    url(../../assets/img/experience-bg.jpg);
  background-position: center 35%;
  background-size: cover;

  display: grid;
  grid-template-columns: 1fr minmax(30%, 80rem) 1fr;

  @include respond(medium) {
    padding: 10rem 5rem;
  }

  @include respond(small) {
    padding: 10rem 3rem;
  }

  &__heading {
    color: $color-primary;
    grid-column: 1 / -1;
  }

  &__card {
    grid-column: 2 / 3;
  }
}
</style>
