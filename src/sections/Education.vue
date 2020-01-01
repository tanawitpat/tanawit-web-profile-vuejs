<template>
  <section class="section-education">
    <h1 class="heading-primary u-margin-bottom-big section-education__heading">Education</h1>
    <div class="section-education__card">
      <EducationCard
        universityName="Chulalongkorn University"
        degree="Bachelor of Science in Statistics"
        honor="Second-Class Honors"
        duration="2014-2018"
        schoolLogoPath="img/chula.png"
        schoolLink="https://www.chula.ac.th/en"
        :descriptions="[
          'Head of Statistics Department Exhibition in Banshi Chula Expo 2017.',
          'Research Assistant at Center of Statistical Consulting and Research, CU.',
          'Teaching Assistant in Data Science Practicum class.'
        ]"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import EducationCard from '../components/EducationCard.vue';

export default {
  name: 'section-education',
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
    rgba(#fff, 0.8)),
    url(../assets/img/education-bg.jpg);
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
