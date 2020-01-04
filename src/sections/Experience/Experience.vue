<template>
  <section class="section-experience">
    <h1 class="heading-primary u-margin-bottom-big section-experience__heading">
      Experience
    </h1>
    <div class="section-experience__card">
      <ExperienceCard
        title="Software Engineer"
        companyName="Central Technology"
        duration="November 2019-Present"
        companyWebsite="http://central.tech"
        description="Exploring the frontend development world."
        companyLogoPath="img/central-tech.png"
      />
      <ExperienceCard
        title="Machine Learning Engineer"
        companyName="Kasikorn Business-Technology Group"
        duration="July 2018-October 2019"
        companyWebsite="http://kbtg.tech/en"
        description="My first journey in software development. I worked with Data Scientists
          to develop machine learning-based services which improved KBank customer experience,
          boosted revenue, and reduced manual processes. The projects covered various areas such as
          credit scoring, OCR, and virtual wallet."
        companyLogoPath="img/kbtg.png"
      />
      <ExperienceCard
        title="Data Scientist Intern"
        companyName="Kasikorn Business-Technology Group"
        duration="June 2017-August 2017"
        companyWebsite="http://kbtg.tech/en"
        description="Applied statistics and machine learning knowledge with real-world business
          problems. Our team identified characteristics of potentially default credit card customers
          and proposed solutions to prevent credit approval for credit card applicants that obtain
          such characteristics. We won 1st place in the internship project competition."
        companyLogoPath="img/kbtg.png"
      />
      <ExperienceCard
        title="Intern"
        companyName="Krungsri Securities"
        duration="June 2016"
        companyWebsite="https://www.krungsrisecurities.com"
        description="Analyzed business performance and financial reports of a company of interest
          and identified its target stock price. I gained a concrete understanding of a capital
          market and investment strategy."
        companyLogoPath="img/krungsri.jpg"
      />
      <ExperienceCard
        title="Sales Professional"
        companyName="Chulalongkorn Business Administration (CBA)"
        duration="May 2015-July 2015"
        companyWebsite="https://www.facebook.com/CBAChula"
        description="Identified consumer needs and set up sales booths in different locations in
          Bangkok. I achieved the sales target within five weeks out of 11 weeks of the program
          period."
        companyLogoPath="img/cba.jpg"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ExperienceCard from './components/ExperienceCard.vue';

export default {
  name: 'section-experience',
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
