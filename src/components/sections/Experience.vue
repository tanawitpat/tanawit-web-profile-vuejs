<template>
  <section class="section-experience">
    <h1 class="heading-primary u-margin-bottom-big section-experience__heading">Experience</h1>
    <div class="section-experience__card">
      <div class="experience-card">
        <h3 class="experience-card__position">Software Engineer (Frontend)</h3>
        <a href="http://central.tech" class="experience-card__company-name">Central Technology</a>
        <p class="experience-card__duration">November 2019-Present</p>
        <a href="http://central.tech"><img src="../../assets/img/central-tech.png" alt="Central Tech logo" class="experience-card__company-logo"></a>
        <p class="experience-card__description">
          Exploring the frontend development world.
        </p>
      </div>
      <div class="experience-card">
        <h3 class="experience-card__position">Machine Learning Engineer</h3>
        <a href="http://kbtg.tech/en" class="experience-card__company-name">Kasikorn Business-Technology Group</a>
        <p class="experience-card__duration">July 2018-October 2019</p>
        <a href="http://kbtg.tech/en"><img src="../../assets/img/kbtg.png" alt="KBTG logo" class="experience-card__company-logo"></a>
        <p class="experience-card__description">
          My first journey in software development. I worked with Data Scientists to develop
          machine learning-based services which improved KBank customer experience, boosted
          revenue, and reduced manual processes. The projects covered various areas such as
          credit scoring, OCR, and virtual wallet.
        </p>
      </div>
      <div class="experience-card">
        <h3 class="experience-card__position">Data Scientist Intern</h3>
        <a href="http://kbtg.tech/en" class="experience-card__company-name">Kasikorn Business-Technology Group</a>
        <p class="experience-card__duration">June 2017-August 2017</p>
        <a href="http://kbtg.tech/en"><img src="../../assets/img/kbtg.png" alt="KBTG logo" class="experience-card__company-logo"></a>
        <p class="experience-card__description">
          Applied statistics and machine learning knowledge with real-world business problems.
          Our team identified characteristics of potentially default credit card customers and
          proposed solutions to prevent credit approval for credit card applicants that obtain
          such characteristics. We won 1st place in the internship project competition.
        </p>
      </div>
      <div class="experience-card">
        <h3 class="experience-card__position">Intern</h3>
        <a href="https://www.krungsrisecurities.com" class="experience-card__company-name">Krungsri Securities</a>
        <p class="experience-card__duration">June 2016</p>
        <a href="https://www.krungsrisecurities.com"><img src="../../assets/img/krungsri.jpg" alt="Krungsri Securities logo" class="experience-card__company-logo"></a>
        <p class="experience-card__description">
          Analyzed business performance and financial reports of a company of interest and
          identified its target stock price. I gained a concrete understanding of a capital
          market and investment strategy.
        </p>
      </div>
      <div class="experience-card">
        <h3 class="experience-card__position">Sales Professional</h3>
        <a href="https://www.facebook.com/CBAChula" class="experience-card__company-name">Chulalongkorn Business Administration (CBA)</a>
        <p class="experience-card__duration">May 2015-July 2015</p>
        <a href="https://www.facebook.com/CBAChula"><img src="../../assets/img/cba.jpg" alt="CBA logo" class="experience-card__company-logo"></a>
        <p class="experience-card__description">
          Identified consumer needs and set up sales booths in different locations in Bangkok.
          I achieved the sales target within five weeks out of 11 weeks of the program period.
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default {
  name: 'section-experience',
};
</script>

<style scoped lang="scss">
.section-experience {
  padding: 10rem;
  position: relative;
  background-image: linear-gradient(
    to right bottom,
    rgba($color-grey-light-1, .9),
    rgba(#fff, .9)),
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
