<template>
  <div class="project-card">
    <h3 class="project-card__name u-center-text">{{ projectName }}</h3>
    <img
      :src="require(`@/assets/${previewImagePath}`)"
      :alt="projectName"
      class="project-card__img"
    />
    <p class="project-card__description">{{ description }}</p>
    <div class="project-card__footer">
      <template v-if="actions.length == 1">
        <div
          :onclick="`window.location='` + actions[0].link + `';`"
          class="project-card__footer__single-button u-center-text"
        >{{ actions[0].label }}</div>
      </template>
      <template v-else-if="actions.length == 2">
        <div
          :onclick="`window.location='`+actions[0].link +`';`"
          class="project-card__footer__double-button project-card__footer__double-button--1 u-center-text"
        >{{ actions[0].label }}</div>
        <div
          :onclick="`window.location='`+actions[1].link +`';`"
          class="project-card__footer__double-button project-card__footer__double-button--2 u-center-text"
        >{{ actions[1].label }}</div>
      </template>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ProjectCard extends Vue {
  @Prop()
  projectName!: string;

  @Prop()
  previewImagePath!: string;

  @Prop()
  description!: string;

  @Prop()
  actions!: object;
}
</script>

<style scoped lang="scss">
.project-card {
  color: #fff;
  border-radius: 20px;

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  overflow: hidden;

  &__name {
    grid-row: 1 / 2;
    grid-column: 1 / 3;
    z-index: 3;
    padding: 1rem 0;
    background-color: rgba(#fff, 0.8);
    color: $color-blue-dark;
    font-weight: bold;
  }

  &__img {
    width: 100%;
    grid-row: 2 / 4;
    grid-column: 1 / 3;
    z-index: 1;

    &:hover ~ p {
      color: black;
      background-color: rgba(#fff, 0.8);

      display: flex;
      align-items: center;
      justify-content: center;
    }
  }

  &__description {
    grid-row: 2 / 4;
    grid-column: 1 / 3;
    z-index: 2;
    padding: 3rem;
    display: none;

    &:hover {
      color: black;
      background-color: rgba(#fff, 0.8);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    @include respond(mobile) {
      display: block;
      color: $color-blue-dark;
      background-color: rgba(#fff, 0.7);
      grid-row: 4 / 5;
      padding: 2rem;
    }
  }

  &__footer {
    grid-row: 4 / 5;

    &__single-button {
      padding: 1rem 0;
      transition: all 0.2s;
      color: $color-blue-dark;
      background-color: rgba(#fff, 0.8);
      font-weight: bold;
      font-size: 1.5rem;
      text-transform: uppercase;
      cursor: pointer;
      grid-column: 1 / 3;

      &:hover,
      &:active {
        color: #fff;
        background-color: rgba(#fff, 0.05);
      }
    }

    &__double-button {
      padding: 1rem 0;
      transition: all 0.2s;
      color: $color-blue-dark;
      background-color: rgba(#fff, 0.8);
      font-weight: bold;
      font-size: 1.5rem;
      text-transform: uppercase;
      cursor: pointer;

      &:hover,
      &:active {
        color: #fff;
        background-color: rgba(#fff, 0.05);
      }

      &--1 {
        grid-column: 1 / 2;
        margin-right: 0.05rem;
      }

      &--2 {
        grid-column: 2 / 3;
        margin-left: 0.05rem;
      }
    }
  }
}
</style>
