<template>
  <section class="section-skills">
    <div class="bg-video">
      <video class="bg-video__content" autoplay muted loop>
        <source src="../../assets/img/Love-Coding.mp4" type="video/mp4">
        <source src="../../assets/img/Love-Coding.webm" type="video/webm">
          Your browser is not supported!
      </video>
    </div>
    <h1 class="heading-primary u-margin-bottom-medium section-skills__heading">Skills</h1>
    <div class="section-skills__cards">
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Frontend Development</h3>
        <div class="section-skills__cards__card--content">
            <div class="skill-card">
              <img src="../../assets/img/skills/javascript.jpg" alt="" class="">
              <p>JavaScript</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/react.png" alt="" class="">
              <p>React</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/vue.png" alt="" class="">
              <p>Vue</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/html.png" alt="" class="">
              <p>HTML</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/css.png" alt="" class="">
              <p>CSS</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/sass.png" alt="" class="">
              <p>SASS</p>
            </div>
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Backend Development</h3>
        <div class="section-skills__cards__card--content">
            <div class="skill-card">
              <img src="../../assets/img/skills/go.png" alt="" class="">
              <p>Go</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/python.png" alt="" class="">
              <p>Python</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/graphql.png" alt="" class="">
              <p>GraphQL</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/mysql.png" alt="" class="">
              <p>MySQL</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/mongodb.png" alt="" class="">
              <p>MongoDB</p>
            </div>
            <div class="skill-card">
              <img src="../../assets/img/skills/redis.png" alt="" class="">
              <p>Redis</p>
            </div>
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">Cloud Services</h3>
        <div class="section-skills__cards__card--content">
          <div class="skill-card">
            <img src="../../assets/img/skills/ec2.png" alt="" class="">
            <p>EC2</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/s3.png" alt="" class="">
            <p>S3</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/route53.png" alt="" class="">
            <p>Route 53</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/gke.png" alt="" class="">
            <p>GKE</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/gcr.png" alt="" class="">
            <p>Google Cloud Run</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/firebase.png" alt="" class="">
            <p>Firebase</p>
          </div>
        </div>
      </div>
      <div class="section-skills__cards__card">
        <h3 class="section-skills__cards__card--topic">DevOps</h3>
        <div class="section-skills__cards__card--content">
          <div class="skill-card">
            <img src="../../assets/img/skills/docker.png" alt="" class="">
            <p>Docker</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/jenkins.png" alt="" class="">
            <p>Jenkins</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/kubernetes.png" alt="" class="">
            <p>Kubernetes</p>
          </div>
          <div class="skill-card">
            <img src="../../assets/img/skills/robotframework.png" alt="" class="">
            <p>Robot Framework</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default {
  name: 'section-skill',
};
</script>

<style scoped lang="scss">
.section-skills {
  padding: 10rem 15rem;
  position: relative;
  background-color: rgba($color-blue-dark, .85);

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
