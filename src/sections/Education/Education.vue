<template>
  <section class="section-education">
    <h1 class="heading-primary u-margin-bottom-big section-education__heading">Education</h1>
    <div class="section-education__card">
      <EducationCard
        v-for="item in educationData"
        :key="item.schoolName"
        :schoolName="item.schoolName "
        :degree="item.degree"
        :honor="item.honor"
        :duration="item.duration"
        :schoolLogoPath="item.schoolLogoPath"
        :schoolLink="item.schoolLink"
        :descriptions="item.descriptions"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import EducationCard from './components/EducationCard.vue';
import educationData from '@/assets/data/education.json';

export default {
  name: 'section-education',
  data() {
    return {
      educationData: educationData.data,
    };
  },
  components: {
    EducationCard,
  },
};
</script>

<style scoped lang="scss">
.section-education {
  background-image: linear-gradient(
      to right bottom,
      rgba(#fff, 0.8),
      rgba(#fff, 0.8)
    ),
    url(../../assets/img/education-bg.jpg);
  background-position: center 35%;
  background-size: cover;

  padding: 10rem;
  position: relative;

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
