<template>
  <section class="section-skills">
    <div class="bg-video">
      <video class="bg-video__content" autoplay muted loop>
        <source src="../../assets/img/Love-Coding.mp4" type="video/mp4" />
        <source src="../../assets/img/Love-Coding.webm" type="video/webm" />
        Your browser is not supported!
      </video>
    </div>
    <h1 class="heading-primary u-margin-bottom-medium section-skills__heading">
      Skills
    </h1>
    <div class="section-skills__cards">
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Frontend Development</h3>
        <div class="section-skills__cards__card--content">
          <SkillCard iconPath="img/skills/javascript.jpg" name="JavaScript" />
          <SkillCard iconPath="img/skills/react.png" name="React" />
          <SkillCard iconPath="img/skills/vue.png" name="Vue" />
          <SkillCard iconPath="img/skills/html.png" name="HTML" />
          <SkillCard iconPath="img/skills/css.png" name="CSS" />
          <SkillCard iconPath="img/skills/sass.png" name="SASS" />
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Backend Development</h3>
        <div class="section-skills__cards__card--content">
          <SkillCard iconPath="img/skills/go.png" name="Go" />
          <SkillCard iconPath="img/skills/python.png" name="Python" />
          <SkillCard iconPath="img/skills/graphql.png" name="GraphQL" />
          <SkillCard iconPath="img/skills/mysql.png" name="MySQL" />
          <SkillCard iconPath="img/skills/mongodb.png" name="MongoDB" />
          <SkillCard iconPath="img/skills/redis.png" name="Redis" />
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Cloud Services</h3>
        <div class="section-skills__cards__card--content">
          <SkillCard iconPath="img/skills/ec2.png" name="EC2" />
          <SkillCard iconPath="img/skills/s3.png" name="ReS3dis" />
          <SkillCard iconPath="img/skills/route53.png" name="Route53" />
          <SkillCard iconPath="img/skills/gke.png" name="GKE" />
          <SkillCard iconPath="img/skills/gcr.png" name="Google Cloud Run" />
          <SkillCard iconPath="img/skills/firebase.png" name="Firebase" />
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">DevOps</h3>
        <div class="section-skills__cards__card--content">
          <SkillCard iconPath="img/skills/docker.png" name="Docker" />
          <SkillCard iconPath="img/skills/jenkins.png" name="Jenkins" />
          <SkillCard iconPath="img/skills/kubernetes.png" name="Kubernetes" />
          <SkillCard
            iconPath="img/skills/robotframework.png"
            name="Robot Framework"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SkillCard from './components/SkillCard.vue';

export default {
  name: 'section-skill',
  components: {
    SkillCard,
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

    &__card {
      text-align: center;

      &:not(:last-child) {
        margin-bottom: 3rem;
      }

      &--topic {
        text-align: center;
        margin-bottom: 3rem;
      }

      &--content {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
      }
    }
  }
}
</style>
