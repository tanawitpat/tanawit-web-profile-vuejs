<template>
  <section class="section-education">
    <h1 class="heading-primary u-margin-bottom-big section-education__heading">Education</h1>
    <div class="section-education__card">
      <div class="education-card">
        <h3 class="education-card__university-name">
          <a href="https://www.chula.ac.th/en">Chulalongkorn University</a>
        </h3>
        <p class="education-card__degree">Bachelor of Science in Statistics</p>
        <p class="education-card__honors">Second-Class Honors</p>
        <p class="education-card__duration">2014-2018</p>
        <a href="https://www.chula.ac.th/en">
          <img
            src="../../assets/img/chula.png"
            alt="Chulalongkorn University logo"
            class="education-card__university-logo"
          >
        </a>
        <ul class="education-card__description">
          <li>Head of Statistics Department Exhibition in Banshi Chula Expo 2017.</li>
          <li>Research Assistant at Center of Statistical Consulting and Research, CU.</li>
          <li>Teaching Assistant in Data Science Practicum class.</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default {
  name: 'section-education',
};
</script>

<style scoped lang="scss">
.section-education {
  background-image: linear-gradient(
      to right bottom,
      rgba(#fff, 0.8),
      rgba(#fff, 0.8)),
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
