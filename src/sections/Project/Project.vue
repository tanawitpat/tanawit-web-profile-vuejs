<template>
  <section class="section-project">
    <h1 class="heading-primary u-margin-bottom-small section-project__heading">
      Personal Projects
    </h1>
    <div class="section-project__quote">
      <p>
        For the things we have to learn before we can do them, we learn by doing
        them.
      </p>
      <p>- Aristotle, The Nicomachean Ethics -</p>
    </div>
    <div class="section-project__card">
      <ProjectCardTwoButton
        projectName="Tanawit's Web Profile"
        previewImagePath="img/project-tanawitp.png"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
          ultrices gravida dictum fusce ut. Velit euismod in pellentesque massa."
        buttonOneLink="https://tanawitp.me"
        buttonOneLabel="Website"
        buttonTwoLink="https://github.com/tanawitpat/tanawitp-frontend-sass"
        buttonTwoLabel="Source Code"
      />
      <ProjectCardTwoButton
        projectName="Kiren BBQ"
        previewImagePath="img/project-kiren.png"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
          ultrices gravida dictum fusce ut. Velit euismod in pellentesque massa."
        buttonOneLink="http://kiren.tanawitp.me"
        buttonOneLabel="Website"
        buttonTwoLink="http://github.com/tanawitpat/kiren-frontend"
        buttonTwoLabel="Source Code"
      />
      <ProjectCardOneButton
        projectName="ML Kubernetes"
        previewImagePath="img/project-ml-kubernetes.png"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
          ultrices gravida dictum fusce ut. Velit euismod in pellentesque massa."
        buttonLink="http://github.com/tanawitpat/ml-kubernetes"
        buttonLabel="Source Code"
      />
    </div>
    <div class="section-project__footer">
      <button
        onclick="window.location='https://github.com/tanawitpat'"
        type="button"
        class="btn"
      >
        Explore more
      </button>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ProjectCardOneButton from './components/ProjectCardOneButton.vue';
import ProjectCardTwoButton from './components/ProjectCardTwoButton.vue';

export default {
  name: 'section-project',
  components: {
    ProjectCardOneButton,
    ProjectCardTwoButton,
  },
};
</script>

<style scoped lang="scss">
.section-project {
  padding: 10rem 15rem;
  background-image: linear-gradient(
      to right bottom,
      rgba($color-blue-dark, 0.9),
      rgba($color-blue-dark, 0.9)
    ),
    url(../../assets/img/bg1.jpg);

  @include respond(medium) {
    padding: 10rem 5rem;
  }

  @include respond(small) {
    padding: 10rem 3rem;
  }

  &__heading {
    color: #fff;
  }

  &__quote {
    color: #fff;
    text-align: center;
    font-size: 1.5rem;
    margin-bottom: 6rem;
  }

  &__card {
    margin-bottom: 6rem;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
    grid-gap: 5rem;
  }

  &__footer {
    text-align: center;

    button.btn {
      border: none;
      color: $color-blue-dark;
      background-color: rgba(#fff, 0.8);
      font-size: 1.6rem;
      font-weight: 600;
      padding: 1.5rem 2.5rem;
      text-transform: uppercase;
      transition: transform 0.2s, background-color 0.2s, color 0.2s;
      cursor: pointer;

      &:hover,
      &:active {
        background-color: rgba(#fff, 0.05);
        color: #fff;
        transform: scale(1.1);
      }
    }
  }
}
</style>
