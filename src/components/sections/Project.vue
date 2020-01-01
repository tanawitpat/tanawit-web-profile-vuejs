<template>
  <section class="section-project">
    <h1 class="heading-primary u-margin-bottom-small section-project__heading">
      Personal Projects
    </h1>
    <div class="section-project__quote">
      <p>For the things we have to learn before we can do them, we learn by doing them.</p>
      <p>- Aristotle, The Nicomachean Ethics -</p>
    </div>
    <div class="section-project__card">
      <div class="project-card">
        <h3 class="project-card__name u-center-text">Tanawit's Web Profile</h3>
        <img
          src="../../assets/img/project-tanawitp.png"
          alt="Tanawit's Web Profile"
          class="project-card__img"
        >
        <p class="project-card__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices
          gravida dictum fusce ut. Velit euismod in pellentesque massa.
        </p>
        <div class="project-card__footer">
            <div
              onclick="window.location='https://tanawitp.me';"
              class="
                project-card__footer__double-button
                project-card__footer__double-button--1
                u-center-text
              "
            >
              Website
            </div>
            <div
              onclick="window.location='https://github.com/tanawitpat/tanawitp-frontend-sass';"
              class="
                project-card__footer__double-button
                project-card__footer__double-button--2
                u-center-text
              "
            >
              Source Code
            </div>
        </div>
      </div>
      <div class="project-card">
        <h3 class="project-card__name u-center-text">Kiren BBQ</h3>
        <img src="../../assets/img/project-kiren.png" alt="Kiren BBQ" class="project-card__img">
        <p class="project-card__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices
          gravida dictum fusce ut. Velit euismod in pellentesque massa.
        </p>
        <div class="project-card__footer">
            <div onclick="window.location='http://kiren.tanawitp.me';" class="project-card__footer__double-button project-card__footer__double-button--1 u-center-text">
              Website
            </div>
            <div onclick="window.location='http://github.com/tanawitpat/kiren-frontend';" class="project-card__footer__double-button project-card__footer__double-button--2 u-center-text">
              Source Code
            </div>
        </div>
      </div>
      <div class="project-card">
        <h3 class="project-card__name u-center-text">ML Kubernetes</h3>
        <img
          src="../../assets/img/project-ml-kubernetes.png"
          alt="ML Kubernetes"
          class="project-card__img"
        >
        <p class="project-card__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices
          gravida dictum fusce ut. Velit euismod in pellentesque massa.
        </p>
        <div class="project-card__footer">
            <div
              onclick="window.location='http://github.com/tanawitpat/ml-kubernetes';"
              class="project-card__footer__single-button u-center-text"
            >
              Source Code
            </div>
        </div>
      </div>
    </div>
    <div class="section-project__footer">
      <button onclick="window.location='https://github.com/tanawitpat'"  type="button" class="btn">
        Explore more
      </button>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default {
  name: 'section-project',
};
</script>

<style scoped lang="scss">
.section-project {
  padding: 10rem 15rem;
  background-image: linear-gradient(
    to right bottom,
    rgba($color-blue-dark, .9),
    rgba($color-blue-dark, .9)),
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
      background-color: rgba(#fff, .8);
      font-size: 1.6rem;
      font-weight: 600;
      padding: 1.5rem 2.5rem;
      text-transform: uppercase;
      transition: transform .2s, background-color .2s, color .2s;
      cursor: pointer;

      &:hover,
      &:active {
        background-color: rgba(#fff, .05);
        color: #fff;
        transform: scale(1.1);
      }
    }
  }
}
</style>
