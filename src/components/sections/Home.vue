<template>
  <section id="section-home" class="section-home">
    <div class="section-home__greeting u-center-text">
      <h1 class="section-home__greeting--message">Hi, I'm Tanawit</h1>
      <div class="section-home__greeting--description">Developer | Data</div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default {
  name: 'section-home',
};
</script>

<style scoped lang="scss">
.section-home {
  background-image: linear-gradient(105deg,
    rgba($color-blue-dark, .9) 0%,
    rgba($color-blue-dark, .9) 50%,
    transparent 50%),
    url(../../assets/img/cover.png);
  background-position: right top;
  background-size: cover;
  height: 95vh;
  padding: 0 5rem;

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  justify-content: center;

  @include respond(large) {
    background-image: url(../../assets/img/cover.png);
    background-position: 90% top;
    grid-template-columns: 1fr;
  }

  &__greeting {
    color: #ddd;
    font-size: 2.5rem;
    animation-name: moveInBottom;
    animation-duration: .8s;
    animation-timing-function: ease-out;
    &--message {
        margin-bottom: .6rem;
    }
    &--description {
        font-size: 2rem;
    }
  }
}
</style>
